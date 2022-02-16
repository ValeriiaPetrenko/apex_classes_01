public class AssignAllTasksOfAccount {
    @InvocableMethod(label='If there are more than 3 tasks, assign them to one user')
    public static void AssignTasks(List<String> ids){
        List<Task> tasks = [SELECT Subject FROM Task WHERE WhatId in :ids];
        List<Account> accs = [SELECT Name FROM Account WHERE Id in :ids];
        for(Account acc :accs){
            if(tasks.size() > 3){
                for(Task ts :tasks){
                    ts.OwnerId = '0057Q000002D0bc';
                }
            }
        }
        update tasks;
    }
}
