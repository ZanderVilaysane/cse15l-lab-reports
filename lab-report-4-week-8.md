# Lab Report 4, Week 8
## Author: Zander Vilaysane
- The following is my own markdown-parse repo: [Matchubi's Repository][Matchubi]
- The following repo was reviewed during Lab 7: [Barakar13's Repository][Barakar]

> Note: I determined expected outputs based off CommonMark's preview of a blue underline like [this][random video] as seen in the following visuals' preview box 

## Snippet 1 Expected Output (via CommonMark)
![Snippet1Expected][snip1]
Snippet 1 considers parsing with conditions of backticks

## Snippet 2 Expected Output (via CommonMark)
![Snippet2Expected][snip2]
Snippet 2 considers parsing with conditions of nested parenthesis/brackets, and escaped brackets

## Snippet 3 Expected Output (via CommonMark)
![Snippet3Expected][snip3]
Snippet 3 considers parsing with conditions of newlines within brackets/parenthesis

## Tests made in my own `MarkdownParseTest.java`
![MarkdownParseTests][TestOutputs]

## My Own Implementation: Snippet 1 Output
![Snip1Output][Output1]
Snippet 1's test **did not pass** due to an `AssertionError`
- Expected one readable link but instead read 3 nested

## My Own Implementation: Snippet 2 Output
![Snip2Output][Output2]
Snippet 2's test **did not pass** due to an `AssertionError`

## My Own Implementation: Snippet 3 Output
![Snip3Output][Output3]
Snippet 3's test **did not pass** due to an `AssertionError`

---

## Tests made in the Reviewed Repo (Barakar13's Tests)
![MarkdownParseTestsReview][TestOutputsReview]

## Reviewed Implementation: Snippet 1 Output
![Snip4Output][Output4]
Snippet 1's test **did not pass** due to an `AssertionError`

## Reviewed Implementation: Snippet 2 Output
![Snip5Output][Output5]
Snippet 2's test **did not pass** due to an `AssertionError`

## Reviewed Implementation: Snippet 3 Output
![Snip6Output][Output6]
Snippet 3's test **did not pass** due to an `AssertionError`

## Code Change Responses:
1. In regards to Snippet 1 and it's inline code w/ backticks, it is possible to make these cases work in a small code change. To make url.com (line 1) readable, we can check to start the parsing after the first closed bracket using the `indexOf` method to make the logic be wrapped my an if condition. 
2. With brackets within the `[]` variable name, we can account for this by checking if there is an even amount of brackets (should be in pairs). This could be checked with a small code change. It should also read the brackets on the outermost layer by comparing the int value using `indexOf`. It should use `[` with the smallest int value and the `]` with the largest int value. 
3. With new line conditions, there may be multiple cases that need to be accounted for as new lines cause our system to not know whene exactly the parser should be concluding it's logic for a link. This can be achieved by checking when `]` is present or not. It's tricky as there may be no closing parenthesis at all but the system woulnd't know when to stop checking when there are links that do exist with a `]` after a few new lines. We can keep track of a counter of the amount of characters/text that exist when reading past `)` searching for a new bracket. 

---
[Matchubi]: https://github.com/matchubi/markdown-parser-ZV
[Barakar]: https://github.com/Barakar13/markdown-parser
[random video]: https://www.youtube.com/watch?v=dQw4w9WgXcQ&ab_channel=RickAstley) 
[snip1]: https://user-images.githubusercontent.com/103156131/169719978-077e97e5-f4f8-40eb-8007-53f5da649035.JPG
[snip2]: https://user-images.githubusercontent.com/103156131/169719992-e0059f42-fba4-4b1d-810c-314debbdd35b.JPG
[snip3]: https://user-images.githubusercontent.com/103156131/169719998-5081b8b7-db2a-474e-92eb-17aa7e145662.JPG
[TestOutputs]: https://user-images.githubusercontent.com/103156131/169719866-fd20e924-0130-4be8-b45e-006408b1d071.JPG
[Output1]: https://user-images.githubusercontent.com/103156131/169719948-14672b4e-0f44-41fd-b901-3924187cdbd0.JPG
[Output2]: https://user-images.githubusercontent.com/103156131/169719960-fea54497-fe18-4040-9f93-4b0df5fa1a3d.JPG
[Output3]: https://user-images.githubusercontent.com/103156131/169719967-4de138d3-2cef-4726-8469-1a8cfa9d3b5e.JPG
[TestOutputsReview]: https://user-images.githubusercontent.com/103156131/169719937-af1c3761-6ec1-4351-b2b6-d6b1aa07c2c9.JPG
[Output4]: https://user-images.githubusercontent.com/103156131/169720074-7fc586d0-2a5e-412c-ab20-97f0a6b4b7cf.JPG
[Output5]: https://user-images.githubusercontent.com/103156131/169720083-d9f78253-0029-47e4-b1fe-5dfb0de977ac.JPG
[Output6]: https://user-images.githubusercontent.com/103156131/169720087-5c958789-98da-4ad0-bdb2-f6d73e05a1df.JPG
