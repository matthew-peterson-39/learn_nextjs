# Optimizing Fonts and Images

# Why Optimize Fonts?

- Fonts are import to the design of a website, however, custom fonts can often affect the performance if the font needs to be fetched and loaded prior to use.

- [Cumulative_Layout_Shift]() is a metirc used by Google to evalute the performance and user experience of a website. With fonts, layoutshift happens when the browswer initially renders the text in a fallbavk or system font then swaps it out for a custom font once it has loaded. This swap can cause the text size, spacing, or layout to change, shifting elements around it.

- Next.js patches this by automaticalling optimizing fonts in the application. It downloads font files at build time and host them with your other statis assests. This means when a user visits your application, there are no additional network resquests that would otherwise impact performance.

- In short, Next.js hosts font files with other statis assests removing the need for addtional network requests.

# Adding a Primary Font

- Import 'Inter' font from the next/font/google module. Then specify the font subset.
