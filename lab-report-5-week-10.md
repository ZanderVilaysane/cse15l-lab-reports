# Lab Report 5, Week 10
## Using Vimdiff for Test Comparisons 
The following repo information is referenced from Jerry Xu's (Group 7 member) repository
To compare different test results, the `vimdiff` command can be used between two repos
![vimdiff][vimdiffSS]
## Vimdiff Output 
The rows highlighted in both files indicate a difference in outcome. The two test results that Jerry had taken notice of was Tests 580 and 496. 
![resultsCompare][resultsCompareSS] 
## Test 580
Click [HERE][test580] to view test-file 580 in the provided repo
Jerry's implementation was correct, whereas the provided repo was not. 
Expected can be seen through this commonmark iteration:
![test580commonmark][test580expectSS]
Provided Repo's Output on Test 580: `[/url]`
Jerry's Output on Test 580: `[]`
## Test 496
Click [HERE][test496] to view test-file 496 in the provided repo
Jerry's implementation was not correct, whereas the provided repo was correct
Expected can be seen through this commonmark iteration:
![test496commonmark][test496expectSS]
Provided Repo's Output on Test 580: `[]`
Jerry's Output on Test 580: `[foo(and(bar)]` 
Jerry's output matches that of the commonmark preview, however, it is not a valid link.
Therefore, the statement should not have listed `foo(and(bar)` as one of the links. 

## Bug in Test 496
The problem with this input of `[link](foo(and(bar))` is the presence of multiple parenthesis. 
Therefore, we can assume the error lies within these lines of code: 
![codeError][codeErrorSS]

The close parenthesis int value is being added multiple times and does not equate to the parser's search for a duo set of `()` and `[]`. It only accounts for a link to be valid only if it has these conditions of close and open brackets/parenthesis. However, it does not consider if the link is valid (perhaps the presence of a `.` to determine it's a link or file. 

---
[vimdiffSS]: https://user-images.githubusercontent.com/103156131/172273911-438cbd84-fae1-423b-a4d7-038f76240eb1.JPG
[resultsCompareSS]: https://user-images.githubusercontent.com/103156131/172273989-5f6cc65f-d9fb-4942-b814-820bc0d531e3.JPG
[test580]: https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/580.md
[test496]: https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/496.md
[test580expectSS]: https://user-images.githubusercontent.com/103156131/172286214-eff2909b-7c8d-4149-92e4-79b4d35397d1.JPG
[test496expectSS]: https://user-images.githubusercontent.com/103156131/172286513-b082e3e6-be93-474b-8f27-25ec5aea78d3.JPG
[codeErrorSS]: https://user-images.githubusercontent.com/103156131/172289415-0334f24d-6ba1-4981-b14b-519e59c36927.JPG
