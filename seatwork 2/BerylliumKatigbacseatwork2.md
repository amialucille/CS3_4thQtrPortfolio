# Seatwork #2 - Getting to know CSS Position and z-index.
### This seatwork will ask you to implement the different CSS position on a given code.
### short link to this .md file is: https://bit.ly/4c61P9K
#### Resources (also found in Khub week 5)
- [4 Minute Youtube Video on CSS Position](https://www.youtube.com/watch?v=YEmdHbQBCSQ)
- [CSS Position Tutorial](https://roycan.github.io/CssPositioningZIndexLab/)

### Instructions: 
1. This is individual submission in khub, but you can work with a partner.  When you submit in khub please place both your names in the submission bin.
2. Guided Activity (30 minutes), please follow what is being required.  

    - Make a copy of this .md file to your Q4 repository and name it as **SectionLNseatwork2.md** example **9LiCruzSeatwork2.md**. Place it in your q4 repository vscode local computer. Committing frequently to your Github repository.  
    - Copy the code below and paste it inside a new file (name it as SectionLNseatwork2.html). Place this file in the same location where the .md file is saved. 
    - Change the content values of the meta tags to your names for author/s and the date today for revised.
    - Please do the following tasks that will ask you to reposition HTML elements then answer the guided question for each task on the .md file. Commit changes to the .md file and to the .html file as well.
    **- This seatwork is worth 20pts and should be submitted by the end of the period** The link to [KHub submission bin](https://khub.mc.pshs.edu.ph/mod/assign/view.php?id=15481).
      - Submit the links to your .md file and .html file.

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="author" content="<your names>" />
  <meta name="revised" content="<date today>" />
  <style>
    body { font-family: Arial, sans-serif; }
    .header, .footer {
      background: lightblue;
      padding: 10px;
    }
    .footer {
       opacity: 0.5;
    }
    .sidebar {
      background: lightgreen;
      width: 150px;
      height: 200px;
    }
    .content {
      background: lightyellow;
      width: 300px;
      height: 200px;
    }    
  </style>
</head>
<body>
  <div class="header">Header</div>
  <div class="sidebar">Sidebar</div>
  <div class="content">Main Content</div>
  <div class="footer">Footer</div>
</body>
</html>
```
### Step 1 (Static vs Relative):

- Add in css ```position: relative; top: 20px; left: 20px;``` to .sidebar.
- Guided Question: What changed compared to the default static positioning? Try to give different values to top and left or you can change it to bottom, right.

  Upon applying the changes to the code, the .sidebar moved down and to the right from its original position. In comparison to static positioning, relative positioning allows movement while still keeping the element in the normal flow, meaning its original space is still preserved.

### Step 2 (Fixed):

- Add in css ```position: fixed; bottom: 0; width: 100%;``` to .footer.
- Guided Question: What happens when you scroll the page? Why does the footer behave differently from position relative?

  With position: fixed, the .footer stays at the bottom of the screen even when scrolling. This is because it is positioned relative to the viewport, not the document flow, unlike relative positioning.

### Step 3 (Absolute):

- Add in css ```position: absolute; top: 66px; left: 200px;``` to .content.
- Guided Question: What is the effect of position: absolute on an element? How is it different from fixed?

  Using position: absolute placed the .content at a fixed location based on its nearest positioned parent. It is removed from the normal flow, so it no longer affects other elements. Unlike fixed, it moves along with its parent when scrolling.

### Step 4 : (Absolute)

- Add in html ```<div class="notice">Notice!</div>``` and include the css below:

```css
.notice {
    position: absolute;
    top: 60px;
    left: 400px;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```

- Give .content a z-index: 1.
- Guided Question: Why does the notice appear on top of the content? What happens if you swap the z‑index values?

  The .notice appears on top of .content because it has a higher z-index. This property controls which element appears in front. If the values are swapped, .content will cover the notice. Setting .content to position: relative allows .notice to be positioned at its top-right corner.

- Challenge: 
    * What changes that you have to do on the code that will position .notice box on the top right corner of the .content box? Please write the code on paper as well (both html and css on the part of .notice and .content).
    * Try to change the position of .content to relative then to fixed. What do you observed each time?
    * What do you observe on about the effect of z-index on .notice and .content boxes?

3. Please answer the following reflection questions (15 minutes)

    a. Could you summarize the differences between the CSS position values (static, relative, absolute, fixed)? 

      Static is the default layout. Relative shifts an element without removing it from flow. Absolute positions an element based on its parent and removes it from flow. Fixed anchors an element to the viewport. Sticky acts like relative until a scroll point, then becomes fixed.

    b. How does absolute positioning depend on its parent element?

      Absolute positioning depends on the nearest parent with a non-static position. If none exists, it uses the body as reference.

    c. How do you differentiate sticky from fixed (you can research on sticky)?

      Sticky scrolls normally until it reaches a set point, then stays fixed. Fixed always stays in the same position on screen.

    d. If you were designing a webpage for a school event, how might you use positioning to highlight important information? Please give concrete examples.

      Positioning helps highlight important content. For example, a fixed “Register” button stays visible, absolute positioning places labels precisely, and sticky can keep reminders visible while scrolling.

