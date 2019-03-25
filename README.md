Tasks to answer in your own README.md that you submit on Canvas:

1.  See logger.log, why is it different from the log to console?
logger.log is different than the log to console because logger.log shows all log messages and the log to console only shows the logs written to the INFO level.

2.  Where does this line come from? FINER org.junit.jupiter.engine.execution.ConditionEvaluator logResult Evaluation of condition [org.junit.jupiter.engine.extension.DisabledCondition] resulted in: ConditionEvaluationResult [enabled = true, reason = '@Disabled is not present']
This line comes from the logger used by JUnit itself. This line is specifically found in the logger file.

3.  What does Assertions.assertThrows do?
assertThrows makes sure an assertion is thrown by the tested function. If an assertion is not thrown, the test f

4.  See TimerException and there are 3 questions
   1.  What is serialVersionUID and why do we need it? (please read on Internet)
   A serialVersionUID is a class version number associated with each serializable class and is used during deserialization to verify that the sender and receiver of a serialized object have loaded classes for that object that are compatible with respect to serialization.
    
   2.  Why do we need to override constructors?
   Custom constructors don't call super constructors by default, so we must overwrite them to ensure they call the super class's constructor correctly.
   
   3.  Why we did not override other Exception methods?
   Because by default we use the super class's methods, so we do not need to overwrite them for the other Exception methods.
   
5.  The Timer.java has a static block static {}, what does it do? (determine when called by debugger)
Timer has a static block because it should only initialize its logger one time. The static block makes sure the code inside it runs one time before any Timer classes are instantiated. This makes sure the logger is properly set up before it is ever used.

6.  What is README.md file format how is it related to bitbucket? (https://confluence.atlassian.com/bitbucketserver/markdown-syntax-guide-776639995.html)
The README file format is a Markdown file, which is a file that can be interpreted by a Markdown interpreter. They are related to bitbucket because they can be found at the root level of a repository or can be found in pull request's descriptions or comments.

7.  Why is the test failing? what do we need to change in Timer? (fix that all tests pass and describe the issue)
The test is failing because before we throw the TimerException, the finally block is executed and a nullPointerException. We need to change what timerNow is initialized to.

8.  What is the actual issue here, what is the sequence of Exceptions and handlers (debug)
The issue is the nullPointerException is thrown and handled before the TimerException is thrown and handled.

9.  Make a printScreen of your eclipse JUnit5 plugin run (JUnit window at the bottom panel)

10.  Make a printScreen of your eclipse Maven test run, with console

11.  What category of Exceptions is TimerException and what is NullPointerException
TimerException is an Exception which is a checked exception. NullPointerException is an unchecked exception because it is thrown automatically.

12.  Push the updated/fixed source code to your own repository.
https://github.com/michaeltwiss/exceptionrunner