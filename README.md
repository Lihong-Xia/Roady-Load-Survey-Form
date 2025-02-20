# An Electric Vehicle Survey Form

This is a survey form designed for freeCodeCamp Certificate-[Responsive Web Design Certification](https://www.freecodecamp.org/learn/2022/responsive-web-design/). In this certification, you'll learn the languages that developers use to build webpages: HTML for content, and CSS for design. 

## Table of contents

- [Overview](#overview)
  - [The project](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The project

The goal of this project is to build a survey form to collect data from users. This project can be a good training of making forms with basic HTML and some CSS. 

User Stories:

1. have an ``h1`` element with an ``id`` of title.
2. #title should not be empty.
3. have a p element with an id of description.
4. #description should not be empty.
5. have a form element with an id of survey-form.
6. have an input element with an id of name.
7. #name should have a type of text.
8. #name should require input.
9. #name should be a descendant of #survey-form.
10. have an input element with an id of email.
11. #email should have a type of email.
12. #email should require input.
13. #email should be a descendant of #survey-form.
14. have an input element with an id of number.
15. #number should be a descendant of #survey-form.
16. #number should have a type of number.
17. #number should have a min attribute with a numeric value.
18. #number should have a max attribute with a numeric value.
19. have a label element with an id of name-label.
20. have a label element with an id of email-label.
21. have a label element with an id of number-label.
22. #name-label should contain text that describes the input.
23. #email-label should contain text that describes the input.
24. #number-label should contain text that describes the input.
25. #name-label should be a descendant of #survey-form.
26. #email-label should be a descendant of #survey-form.
27. #number-label should be a descendant of #survey-form.
28. #name should have a placeholder attribute and value.
29. #email should have a placeholder attribute and value.
30. #number should have a placeholder attribute and value.
31. have a select field with an id of dropdown.
32. #dropdown should have at least two selectable (not disabled) option elements.
33. #dropdown should be a descendant of #survey-form.
34. have at least two input elements with a type of radio (radio buttons).
35. have at least two radio buttons that are descendants of #survey-form.
36. all radio buttons should have a value attribute and value.
37. all radio buttons should have a name attribute and value.
38. every radio button group should have at least 2 radio buttons.
39. have at least two input elements with a type of checkbox (checkboxes) that are descendants of #survey-form.
40. all checkboxes inside #survey-form should have a value attribute and value.
41. have at least one textarea element that is a descendant of #survey-form.
42. have an input or button element with an id of submit.
43. #submit should have a type of submit.
44. #submit should be a descendant of #survey-form.

### Screenshot

![](./images/presentation.png)

### Links

- Solution URL: https://github.com/Lihong-Xia/Roady-Load-Survey-Form
- Live Site URL: https://lihong-xia.github.io/Roady-Load-Survey-Form/

## My process

### Built with
- Semantic HTML5 markup
- CSS custom properties
- Figma design file

### What I learned
In my design, I met with several problems. Through searching online and self-reflection I tried to fix these problems.

- First, the heading has two fonts and two colors. I didn't know how to set two styles in the same line. So I went online to search if there is an element that can select part of the content for that I can style the selected content. I found the inline-level element ``span`` can be used to select content for styling purpose. (check the article in [Useful resources](#useful-resources))

- When I was adding radio buttons and checkboxes, I found they didn't stay in the same line as their labels. 

At first I kept input elements and labels as separate elements and wrapped them in a parent ``div`` and used CSS to align them. I set ``display`` property to ``inline-block``. It didn't work. 
Then I tried to wrap the input elements in their corresponding labels. It worked but labels stayed much below radio buttons and checkboxes and I couldn't change the position of labels. 
So I still went back to the first version (keep them as seperate elements). I set background color for labels and found they still looked like block even they are set to ``inline-block``. Then I tried to set the ``width`` of labels to ``auto`` and it worked. They stayed in same lines. But labels stayed much below radio buttons and checkboxes. I tried to change the ``padding`` and ``margin``. At last I set value for the top ``margin`` of radio buttons and checkboxes and it worked. 
Visually they are still not vertically aligned even the ``vertical-align`` property of labels is set to ``middle``. At last I changed the value to ``top`` and visually they are aligned. It's not perfectly aligned and I will try to improve it in the future.

- After I finished all the styling part in CSS I found the text, email, age input and textarea are longer than other elements. I tried many ways but I still failed to change the width. I searched online and I found it's the problem of ``box-sizing`` (read more in [Useful resources](#useful-resources)). I set the value to ``border-box`` and it worked. It's better to apply ``box-sizing`` with a value of ``border-box`` to all the elements at the start of CSS with universal selector (*).

In the future I will design for the mobile version and darkness version of the survey form.

### Useful resources

-[<span>: The Content Span element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/span) - This helped me to style inline.
-[box-sizing](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing) - This helped me to change the size of input box.

## Author

- Email - 
- freeCodeCamp - 