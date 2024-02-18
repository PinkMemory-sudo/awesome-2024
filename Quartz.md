？

* 调度器得作用
* JobDetail与Job的关系，每次执行创建新的Job



方法由调度器的一个线程执行



**JobDetail**

用来设置Job的属性，传递参数

*JobDataMap*

 store state information



Jobs can be created and stored in the job scheduler independent of a trigger, and many triggers can be associated with the same job.





**Why Jobs AND Triggers?** 





Notice that we give the scheduler a JobDetail instance, and that it knows the type of job to be executed by simply providing the job’s class as we build the JobDetail. Each (and every) time the scheduler executes the job, it creates a new instance of the class before calling its execute(..) method





### JobDataMap

这样Job必须有一个无参构造方法，并且数据无法传递





定义JobDetail时将数据放入

```java
 // define the job and tie it to our DumbJob class
  JobDetail job = newJob(DumbJob.class)
      .withIdentity("myJob", "group1") // name "myJob", group "group1"
      .usingJobData("jobSays", "Hello World!")
      .usingJobData("myFloatValue", 3.141f)
      .build();
```





在任务中获得

```java
public class DumbJob implements Job {

    public DumbJob() {
    }

    public void execute(JobExecutionContext context)
      throws JobExecutionException
    {
      JobKey key = context.getJobDetail().getKey();

      JobDataMap dataMap = context.getJobDetail().getJobDataMap();

      String jobSays = dataMap.getString("jobSays");
      float myFloatValue = dataMap.getFloat("myFloatValue");

      System.err.println("Instance " + key + " of DumbJob says: " + jobSays + ", and val is: " + myFloatValue);
    }
  }
```





如果你在job类中，为JobDataMap中存储的数据的key增加set方法（如在上面示例中，增加setJobSays(String val)方法），那么Quartz的默认JobFactory实现在job被实例化的时候会自动调用这些set方法，这样你就不需要在execute()方法中显式地从map中取数据了。





JobExecutionContext中的JobDataMap为我们提供了很多的便利。它是JobDetail中的JobDataMap和Trigger中的JobDataMap的并集，但是如果存在相同的数据，则后者会覆盖前者的值。





@PersistJobDataAfterExecution



### Misfire策略







https://xuzongbao.gitbooks.io/quartz/content/JobStores.html