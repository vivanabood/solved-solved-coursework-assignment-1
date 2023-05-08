Download Link: https://assignmentchef.com/product/solved-solved-coursework-assignment-1
<br>
<p title="CourseWork Assignment 1 Solution">



<p class="ui header product-top-header" title="CourseWork Assignment 1 Solution">IntroductionQuestion (1) asks that you demonstrate an understanding of simple graphics, innerclasses, events and the ActionListener interface. Question (2) looks at the object-orientedprogramming paradigm: inheritance, interfaces, classes (including abstract classes) andinstance methods.

IMPORTANT NOTE: Please use Java 8.

Electronic files you should have:Question (1)• RectanglesGUI.java

Question (2)• BaseQuiz.java• FreeQuiz.java• MultipleChoiceQuiz.java – getQuestions method only• TrueFalseQuiz.java – getQuestions method only• Question.java• FreeQuizQuestion.java• MultipleChoiceQuestion.java• GenericQuizClasses.pdf

Please ensure that you hand in electronic versions of your .java files. Class files are not needed.No zip or compressed files.You are asked to give your classes certain names; please follow these instructions very carefully. Make sure there is no conflict between your file name and your class name.Remember that if you give your files names that are different from the names of your classes (e.g. cwk1-partA.java file name versus RectanglesGUI class name) your program will not compile because of the conflict between the file name and the class name.Compile and run the RectanglesGUI class. You should note that it uses an inner class to place a JPanel onto a JFrame. Some coloured rectangles are drawn on the JPanel:

Output of the RectanglesGUI class

Please complete the following tasks:

1. Shorten the paintComponent (Graphics) method by rewriting the statementsto draw and fill the rectangles with colour. Put the statements into a loop ofyour choosing. The model answer uses nested for loops, and has reduced the number of statements needed to draw the rectangles to 5.2. Using getWidth() and getHeight() for the RectangleDrawPanel, distributethe rectangles evenly across the drawPanel, so that each is fully visible andso that all of the available space is used (see the image below).NOTE: your solution must be scalable – that is, the dimensions of theJFrame could be changed to be bigger or smaller, and the rectangleswould still all be visible and fill the available space, without any otherchanges being made.3. Add a JButton to the SOUTH region of the JFrame using BorderLayout (2 marks). Set the text on the button. The text should invite the user to click the button.4. Write an inner class called RandomColorListener to implement theActionListener interface and to listen to the JButton in the SOUTH region.NOTE: you can only get full credit for this part of the question by writing an inner class.5. When the user clicks on the JButton in the SOUTH region, the rectanglesfilled with color1 should all change to a random Color, while the rectangles filled with color2 should not change. A second click on the JButton should make the rectangles filled with color2 all change to a random Color, while the rectangles filled with a random Color by the first click should stay the same Color. The user should be able to continue clicking on the button indefinitely, and with each click one set of rectangles will be filled with a random Color. In each case, the rectangles to change should be the ones that stayed the same on the last click (in other words, the Color change should alternate between the two sets of rectangles). This means that with each click only one set of rectangles should change colour.6. Write a second inner class implementation of the ActionListener interface,called ResetListener. The ActionPerformed(ActionEvent) method of the class should have a means of resetting the colours of the rectangles back to the colours that they were filled with at the start (orange and blue).7. Add a second JButton to the NORTH region, and add theResetListener to it such that when the button is clicked the rectangles are once again filled with orange and blue, as they were at the start of the program. Further clicks on the button will have no effect when the default orange and blue colours are displayed, but will reset the colours to the default setting once more if they have been changed by clicking the other button. Add an appropriate message to the button telling the user what it does.Output of the RectanglesGUI class, revised so that the rectangles are all thesame size and divide up the available space between them.

Reading for Question (1)• See: <a href="https://docs.oracle.com/javase/7/docs/api/java/awt/Color.html" target="_blank" rel="nofollow noopener">http://docs.oracle.com/javase/7/docs/api/java/awt/Color.html</a> for theconstructors, for example Color(int r, int g, int b), that allow developers to maketheir own Colors.• Chapter 12 of Head First Java, pages 353–81.

Deliverable for Question (1)• An electronic copy of your revised program: RectanglesGUI.java

Question (2)In this part of the coursework assignment, you have been given the BaseQuiz and the FreeQuiz classes, together with the Question, FreeQuizQuestion andMultipleChoiceQuestion classes. BaseQuiz is abstract, and FreeQuiz is one possible concrete class extension of it. You should compile and run the FreeQuiz class and see how it behaves. The FreeQuiz class uses FreeQuizQuestion objects, which are placed into an ArrayList of potential questions. The number of possible questions to be randomly chosen from this ArrayList and asked of the user is set in the getQuizSize() method. You might want to try changing the value (currently 5) a few times to see what happens.

The FreeQuizQuestion class is a child class of the Question class. The Question class specifies that the question itself will be a String, but it does not set the type of answer, which is left to the child classes. FreeQuizQuestion answers are Strings, while the MultipleChoiceQuestion class answers are more complicated. Multiple choice questions need a list of possible answers, and a record of the correct answer. In the MultipleChoiceQuestion class the possible answers are stored in an array, and the actual answer is recorded as an int that holds the position of the correct answer in the list of possible answers; the list of possible answers are numbered starting at 1. Hence in the question:MultipleChoiceQuestion q1 = new MultipleChoiceQuestion(“What isthe primitive data type that starts with ‘i’?”, 1, “int”,“INT”, “Int”, “Integer”); the ‘1’ means that “int” is the correct answer.

You have been given the MultipleChoiceQuiz and TrueFalseQuiz classes; each contains only the populateList() method.

You have been given a PDF with some Generic classes. These classes,GenericBaseQuiz, GenericQuestion, GenericFreeQuiz and GenericFreeQuizQuestion have been adapted from the BaseQuiz, Question, FreeQuiz and FreeQuizQuestion classes respectively.

Please complete the following tasks:

1. Complete the MultipleChoiceQuiz class as a direct child class of BaseQuiz. Include a main method in your class with test statements to make and run an instance of the class. Your completed class should behave in the same way as the FreeQuiz class, except that the questions that it is asking are multiple-choice ones. This means that the question is displayed with a numbered list of possible answers, and the user has to type in the number of the answer that they think is correct. See the Appendix for an example of the output of this class.2. Write the TrueFalseQuestion class as a direct sub-class of theQuestion class.3. Complete the TrueFalseQuiz class as a direct child class of BaseQuiz. Include a main method in your class with test statements to make and run an instance of the class. Your completed class should behave in the same way as the FreeQuiz class, except that the questions that it is asking are true or false. This means that the user is shown a statement and has to decide whether they think the statement is true or false, typing in their answer. See the Appendix for an example of the output of this class.4. Can you explain how and why the Generic classes are different from the classes that they have been based on?

Consider the getRandomQuestions(List, int) method in the GenericBaseQuiz class. The corresponding method was static in BaseQuiz, but is an instance method in GenericBaseQuiz. Can you explain why?

You should write no more than two paragraphs in answer to this question (note a paragraph is at most 8 sentences). You may give in your answer as a PDF, Word, OpenOffice or text file.

Reading for Question (2)The following topics from Head First Java• Object programming• Object behavior• The Java library• Inheritance• Abstraction

Reading for Question 4:• <a href="https://docs.oracle.com/javase/tutorial/java/generics/" target="_blank" rel="nofollow noopener">https://docs.oracle.com/javase/tutorial/java/generics/</a>

Deliverables for Question (2)

Please hand in an electronic copy of the following:• Your completed MultipleChoiceQuiz.java• TrueFalseQuestion.java• Your completed TrueFalseQuiz.java• A PDF, Word, OpenOffice or text file with your answer to Question (2) Part 4(b).

Appendix

Sample output of the completed MultipleChoiceQuiz class (questions randomly chosen)

This quiz has 3 questions. Good luck.QUESTION (6 possible answers): What is the minimum value ofthe byte data type?1. -632. -643. -127 4. -128 5. -2556. -256Enter a number 4QUESTION (3 possible answers): What is the value of theexpression “James”.charAt(“James”.length() – 1) ?1. no value, run-time error2. e3. sEnter a number 3QUESTION (6 possible answers): What is the maximum value ofthe byte data type?1. 632. 643. 127 4. 128 5. 2556. 256Enter a number 3You scored 3/3. That’s 100%. Excellent!

Sample output of the completed TrueFalseQuiz class (questions randomly chosen)

This quiz has 5 questions. Good luck.True or false? Static methods can operate on instancevariables; trueTrue or false? Instance variables hold the same value forevery instance of the class; trueTrue or false? Static methods can be run before an instanceof the class is made; trueTrue or false? Java is case sensitive; trueTrue or false? The following expression type checks: int x =“elf”.compareTo(“7”)+11; falseYou scored 2/5. That’s 40%. You’ll have better days.