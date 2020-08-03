# Tips to program more effectively as a data scientist

## Lessons I learned the hard way my first software project 

Recently, I developed code to automate a mission-critical, but time-intensive, task in R. The end result was successful, but the journey to that result was fraught with painful and stress-inducing debug cycles as the code grew in complexity. 

While I did some things well, in particular

- Documenting code by using expressive variable and function names, and leaving comments
- Writing modular code by giving each function a clear and focused use case

I could have developed my code more effectively in an number of ways. Here is some practical programming advice, so that you don't experience the same mistakes I made. 

## Here were some things I should have done better

- Issues primarily related to organization and project hygiene
- Also related to data validation

### Maintain a clear blueprint/mental map of your software design

When I started my software project, I dove into coding with limited upfront planning, thinking that the exact details of my software design would become clearer as I coded.  As my code became more complex and requirements for the code were updated, I started losing track of how all my functions fit together. 

Without a blueprint or diagram to refer to, I invested precious time re-reading code to recall how data was passed to and fro and in what format, and to refresh on the logic I used to manipulate the data.

To avoid this pitfall, I highly suggest having a simple, but clear picture of what your software does at a high-level. A pen-and-paper diagram with boxes and arrows should suffice. This will give you a quick reference to see where you need to make modifications in your code. 

Pay careful attention to the logic of your data manipulations. For complex data manipulations, explicitly state what your intent is and what kind of data processing you are doing, and how it will give you your intended result. This illuminate potential shortcomings of your data logic, and key you in to future catch cases. 

### Investing in a clear file organization

As you write code across several scripts and validate with dozens of Excel files, it will become increasingly challenging. 

- Many files
- Result in scrolling and wasted mental effort trying to find files
- Containing messiness will reduce cognitive load and stress
- Have a consistent, predefined file structure
- Must-haves
    - Folder for the project
    - Naming convention for code
    - Naming convention for data
- Options
    - Use versions (ie _v1, _v2)
    - Include dates - YYYY_MM_DD


### Not designing code to make it easy to check your data at each step

- Ties into idea of creating modular code
- Each time your data is processed, you want be able to get outputs


### Check data inputs and outputs automatically at each step of your code

- This should be done automatically as much as possible
- I spent a lot of time exporting to Excel, building pivots
- Write code that makes it quick once, investing time and mental effor here pays itself back tenfold

### Keep a solutions log

- Keep details of solution so you don't have to debug the same problem twice
- Keep track of each error you face, perhaps in an Excel 
- Suggestion: date of problem, description or error code, solution


### Document changes made to your code

- Especially big problem as you're getting tired
- Keep a log 
- Suggestion
    - Keep this in an Excel log

### Being methodical and composed while debugging

- Often would step through the entire code
- Approach debugging a clear mind
- Suggestion
    - Build context: If there is an error message, invest in understanding it
        - Check that form of inputs are correct, going into problem module 
    - Reduce search space: Isolate out modules in which error is occurring
        - Reduces stress
    - Know what the problem actually is
