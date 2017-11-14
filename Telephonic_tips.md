### Telephonic tips

1. Repeat the question (reword/simplify if needed)

2. Ask clarifying questions about the problem statement
    e.g. Sorted, Duplicate in inputs, Duplicate in output, Input/Output Format, Universe / Range of Input, .

3. Think of various inputs and corner test cases
    e.g. Empty string / NULL input, Duplicates, 0, Variable overflows, Worst Case Input

4. Verify your understanding by verbally confirming few test cases. Extra points if you can first take a simple test case and modify it to come up with a better test case.

5. Establish brute force method. Briefly explain approach and complexity. Extra points if you can communicate why you think a better solution than brute force could exist.

6. Talk properties / obervations noticed in the question and how you are using those to think of various data structures/algorithms. 
    + Try to relate with some trivial data structure / algorithm / problem you solved elsewhere.
    + Communicate what you are thinking and Why do you think it can be used for this question!?

7. Formally communicate your final solution. Do complextiy analysis. 
    + Ask if the solution is indeed correct. If incorrect, ask for hint and jump back to step 6. Make sure you use the hint - they almost always give the best hints. 
    + Once you get it correct, ask if you should code the solution. While coding, Make sure you keep the conversation going. Build the code in modules and tell the interviewer what you will be doing before every module / 2-3 lines of code. 
    + Finally take a non-trivial test case and do a dry run over the code you have written. (Extra points if you can quickly talk through other possible input variations while going through the code pieces)


## Example

### Given a string, find the first missing character.

1. Repeat the question (reword/simplify if needed)
    - "So we will be provided a string as input and we have to find the first character that is missing"

2. Ask clarifying questions about the problem statement
    e.g. Sorted, Duplicate in inputs, Duplicate in output, Input/Output Format, Universe / Range of Input, .
    - "What is the character set?" -> A-Z
    - "Will we get A-Z in both cases?" -> only upper cases
    - "When we say first character, Do we mean alphabatically the smallest character?" -> yes
    - "Is there a gaurantee that atleast 1 character will be missing?" -> NO
    - "What do we return if no character is missing?" -> return the character null

3. Think of various inputs and corner test cases
    e.g. Empty string / NULL input, Duplicates, 0, Variable overflows, Worst Case Input
    - "ABCDEFGHIJKLMNOPQRSTUVWXYZ" -> '\0'
    - "" -> A
    - "HGFEDBA" -> C
    - "ADE" -> B
    - "ABCDEFGHIJKLMNOPQRSTUVWXYA" -> Z

4. Verify your understanding by verbally confirming few test cases. Extra points if you can first take a simple test case and modify it to come up with a better test case.
    - "So say our input is ABDE, since C is missing - our output here should be C. But if the input were ADE, our output would be B since that is the first missing character."

5. Establish brute force method. Briefly explain approach and complexity. Extra points if you can communicate why you think a better solution than brute force could exist.
    - "One simple way or the brute force way to solve this would be to pick every character from A-Z and search for that character in the string. Return the first character that is not found, null otherwise."
    - "This will take O(1) memory since we are not storing any information"
    - "and O(26 N) time since for each character we are going through the whole array once"
    - "The problem is we are parsing the whole array way too many times. If the character set was not a constant and in order of input N, the time complexity would be O(n^2) which is not that great. "

6. Talk properties / obervations noticed in the question and how you are using those to think of various data structures/algorithms. 
    + Try to relate with some trivial data structure / algorithm / problem you solved elsewhere.
    + Communicate what you are thinking and Why do you think it can be used for this question!?

    - "What I am thinking is that since we know the range of the data set, we should be able to use this information to optimize our algorithm"
    - "This seems like an application of HashTable data structure. If we keep the count of how many times each character appeared, we can simply go through the hashmap in alphabatical order and print the first missing character"
    - "Infact we dont even need to keep a count. We can simply keep a hashmap of boolean values"

7. Formally communicate your final solution. Do complextiy analysis. 
    + Ask if the solution is indeed correct. If incorrect, ask for hint and jump back to step 6. Make sure you use the hint - they almost always give the best hints. 
    + Once you get it correct, ask if you should code the solution. While coding, Make sure you keep the conversation going. Build the code in modules and tell the interviewer what you will be doing before every module / 2-3 lines of code. 
    + Finally take a non-trivial test case and do a dry run over the code you have written. (Extra points if you can quickly talk through other possible input variations while going through the code pieces)


### Questions to ask

1. Can you tell about the kind of work interns get and the kind of impact it can lead to.
2. Why XYZ over other companies like ABC, DEF. Top 3 things that you'll tell anyone.
3. How long have you been here and how has your experience been with he company?
4. Can you tell me about the bootcamp / onboarding process? Do we get to select our teams and projects we want to work on.
5. What is the management style of potential boss or the general values of the team?
6. What are the company’s or team’s metrics for success?
7. What’s valued more: team collaboration or hard tech skills?
8. Ask for interviewer to describe what part of the platform you’d be working on
9. Show you listened: “I remember you saying XYZ, and I have a follow up question about that…”


- Make a flowchart - https://www.draw.io/