# Optimizing Fonts and Images

# Why Optimize Fonts?

- Fonts are import to the design of a website, however, custom fonts can often affect the performance if the font needs to be fetched and loaded prior to use.

- [Cumulative_Layout_Shift]() is a metirc used by Google to evalute the performance and user experience of a website. With fonts, layoutshift happens when the browswer initially renders the text in a fallbavk or system font then swaps it out for a custom font once it has loaded. This swap can cause the text size, spacing, or layout to change, shifting elements around it.

- Next.js patches this by automaticalling optimizing fonts in the application. It downloads font files at build time and host them with your other statis assests. This means when a user visits your application, there are no additional network resquests that would otherwise impact performance.

- In short, Next.js hosts font files with other statis assests removing the need for addtional network requests.

# Adding a Primary Font

- Import 'Inter' font from the next/font/google module. Then specify the font subset.

# Why Optimize Images?

- Next.js helps to optimize images by ensuring the Developer does not have to manually ensure the image is responsive on different screen sizes, specify the image size for different devices, prevent layout shift as the images loads, or lazy load images that are outside the uesr's viewport.

- using next/image component automatically optimize images

# The \<Image> Component

- This component is an extension of the HTML \<img> element.

- When using the \<Image> element, it is good practice to set the width and height of your images to avoid layout shift, these should be an aspect ratio identical to the source image.

- The class 'hidden' is used to remobe the image from the DOM on mobile screens.

- The 'md:block' class shows the image on desktop screens.

- To implement the /hero-mobile.png to display for mobile devices, I copied pasted the previous \<Image> element, changed the source to /hero-mobile.png, updated the width and height, and styled it using 'block md:hidden' to ensure it is only displayed on mobile screens.

- T/F : Images without dimesnions and wbe fonts are common causes of layout shfit due to the browswer having to download additional resources... True!