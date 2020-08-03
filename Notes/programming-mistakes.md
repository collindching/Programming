# Tips to program more effectively as a data scientist

Write out remainder
Add examples, pictures, diagrams to explain advice.

## Lessons I learned the hard way my first software project 

Recently, I developed code to automate a mission-critical, but time-intensive, task in R. The end result was successful, but the journey to that result was fraught with painful and stress-inducing debug cycles as the code grew in complexity. 

While I did some things well, in particular

- Documented code well: Via meaningful variable and function names, and writing short explanatory comments
- Writing modular code: Gave each function a clear, focused use case
- Achieved the final goal: At the end of the day, managed to get the necessary output

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

During my project, I severely underestimated the number of files that I would be managing. So as I used more scripts and Excel files, each named and organized loosely according to ad-hoc rules, locating files that I needed became a huge headache. 

If I had simply invested upfront in maintaining a folder hierarchy and following a consistent file naming convention, I would have saved many crucial minutes scrolling through folders to pinpoint files. More importantly, I'd reduce my cognitive load and stress, and have a neat record of all the work I'd previously done.

My suggestion: before starting your project, predefine organization and naming rules for your file structure, rather than coming up with logic on the fly. This will allow you to be as consistent as possible, and limit the amount of cognitive load you have to manage as you get more and more files. 

Some must-haves for file organization, are having a folder for the project, a naming convention for the code, and a naming convention for your data files. For all file types, I recommend adding a date suffix for each file (ie `file_name_2020_08_03`). The advantage is keeping a chronological record of all the files you've used. If you create multiple versions of the same file in one day, use versioning prefixes (ie `v2_file_name_2020_08_03`).

### Check data inputs and outputs automatically at each step of your code

Debugging was by far the most painful part of my software project, especially because I was passing multipel different formats of the same data between different functions. 

To catch unexpected behavior more quickly, and be able to do quick on-the-spot validation of my code, it's best to allow your code to get outputs of your resulting data at each processing step. 

Unit testing works, or you can simply output a summary of results at each stage, which you can use to compare against known numbers. WIth this strategy, you can quickly see if any data is getting lost or corrupted, and at which data data processing step that it's occurring 
at. 

This should be as automated as possible, and you should limit the number of repeated manual operations you run during validation. If you see yourself repeating the same work over and over, you should plan how to automate that process -- either within your code, or via an Excel template. Time invested in automation pays itself back tenfold, likely even more. 

### Keep a solutions log

The same bugs will often pop up in your code, and to avoid researching the same issues over and over again, I recommend tracking the solutions you've used.

By keeping the details of previously used solutions, you keep a growing log of issues that keeps you from repeating efforts with stuff. 

My suggestion is to keep track of each error you face in a Google sheet, and keep it simple. Include the date of the problem, your error code and where it occurred, and the solution that you ended up using. 

### Document changes made to your code

- Especially big problem as you're getting tired
- Keep a log 
- Suggestion
    - Keep this in an Excel log

### Debug systematically

- Following intuition can give you good results, but is an expensive strategy in the long-run 
- Better to have a systematic and methodical approach
- Suggested approach
    - Build context: If there is an error message, invest in understanding it
        - Check that form of inputs are correct, going into problem module 
    - Reduce search space: Isolate out modules in which error is occurring
        - Reduces stress
    - Record hypotheses, test, and record
        - Some initial ideas -- check for unexpected inputs, mismatched data types, or null values
    - Fix and re-run
