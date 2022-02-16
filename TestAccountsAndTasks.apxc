public class TestAccountsAndTasks {
	@InvocableMethod(label='Create task when account was created')
        public static void createTask(List<String> ids){
            List<Task> tasks = new List<Task>();
            List<Account> accs = [SELECT Name FROM Account WHERE Id in :ids];
            for(Account acc :accs){
                Task newtask = new Task(Subject='Negotiations with ' + acc.Name, WhatId=acc.Id);
                tasks.add(newtask);
            }
            insert tasks;
        }
}
