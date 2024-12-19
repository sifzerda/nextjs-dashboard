## Next.js App Router Course - Starter

```bash
https://nextjs.org/learn
```

This is the starter template for the Next.js App Router Course. It contains the starting code for the dashboard application.

For more information, see the [course curriculum](https://nextjs.org/learn) on the Next.js Website.





You can import global.css to any component, but by default should import it into your top-level component, which is the root layout file (layout.js/ts)




When you make a next.js app you can opt to use Tailwind. The CSS will be part of the jsx. If you want to keep the CSS separate and customize your selectors and classes, you can use CSS modules. The css files will be called things like 'home.module.css'.

Create a module.css file (and put inside a sub-folder, e.g. app/styles). Import this into page.ts and create the element bracketing the filename. For instance, inside your module.css file add a class:

```bash
.shape {
  height: 0;
  width: 0;
  border-bottom: 30px solid black;
  border-left: 20px solid transparent;
  border-right: 20px solid transparent;
}
```

Then where you want this element to go, write:

```bash 
<div className={styles.shape} />
```

## Class state toggling:

You can npm install clsx and use to apply conditional classes based on state. For instance inside a page.ts:

```bash
import clsx from 'clsx';

      className={clsx(
        'inline-flex items-center rounded-full px-2 py-1 text-sm',
        {
          'bg-gray-100 text-gray-500': status === 'pending',
          'bg-green-500 text-white': status === 'paid',
        },
```

Other css you can use with Next:
+ Sass (scss files)
+ CSS-in-JS (styled-jsx, styled-components, emotion)

## 
Next uses file-system routing, so folder structure/layout creates the nested routes.

Next creates a default homepage, called app/page.tsx. Other routes and pages can branch out from it.

To create a new page, make a folder in app, and add a page.tsx/js inside. The pathname of the page will be based on the folder structure, e.g:

```bash 
app/dashboard/profile/page.tsx will be found at pathname:

www.[...]dashboard/profile
```

## SHARING LAYOUT BETWEEN PAGES

Anytime you want to share layout between pages, you can make a layout.tsx page to bring in shared components, e.g. a navbar, header, footer, etc. Anything that will display on multiple pages.

In this app, the components are stored inside app/ui/dashboard


