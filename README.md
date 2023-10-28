# CSE2102-Lab5
REST endpoints created for checking validity of passwords and emails via URL RequestParam inputs against hard-coded passwords and emails, and the unformatted output of hard-coded quiz questions.
Three REST Controllers are created to either use a validator class to process and validate a record type (password, email), or a service class is made to create and get the hard-coded  questions (quiz); where the questions are record types as well.

The REST Controllers and their associated files are:

    REST CONTROLLER         : RECORD TYPE                    CLASS/RECORD HANDLER
    PasswordController.java : PasswordValidationResult.java  PasswordValidator.java
    EmailController.java    : EmailValidationResult.java     EmailValidator.java
    QuizController.java     : QuizQuestions.java             QuizService.java

The REST endpoints associated with each REST Controller are:

    REST CONTROLLER         : ENDPOINTS
    PasswordController.java : /password/check
    EmailController.java    : /email/check
    QuizController.java     : /quiz/questions

The REST endpoints for the password and email controllers take in URL parameters for their respective validator classes to process:

    http://localhost:8094/<TYPE>/check?<TYPE>=<INPUT>

Dissimilarly, the endpoint for the quiz controller does not take any parameters, as the hard-coded questions are simply shown unformatted when accessing:

    http://localhost:8094/quiz/questions


INSTRUCTIONS:

1) Download the demolab5.zip file and extract contacts into a target directory
2) Open terminal/console and navigate to root directory of project (~/<TARGET DIRECTORY>/demo/)
3) Input commands to run Spring Boot and enter in browser search bar either of the abovementioned links with their appropriate endpoints and parameters.

       ./.mvnw spring-boot:run
   
