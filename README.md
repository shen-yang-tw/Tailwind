# [Tailwind Toolbox](https://www.tailwindtoolbox.com/) - [Starter Template](https://www.tailwindtoolbox.com/setup)

It's pretty straight forward to setup [Tailwind CSS](https://www.tailwindcss.com/) and give it a test spin using the CDN version. However, as mentioned on the Tailwind site, you need to setup Tailwind using npm in order to start customising Tailwind.

*Note: This starter template is for Tailwind CSS version 1 beta 3 (which is pretty much the [final version](https://twitter.com/adamwathan/status/1108450684783849472))

If you want the starter template for version 0.7.4, then please [download it from here](https://github.com/tailwindtoolbox/StarterTemplate/archive/v0-7-4.zip)*

## Setup Guide
* Download [Node/npm](https://nodejs.org/en/download/)
* Download the [Tailwind Starter Template](https://github.com/tailwindtoolbox/StarterTemplate/archive/master.zip)
* Open ```package.json``` and then edit the follow section of the file to match your project

```"name": "TailwindStarterTemplate",
"version": "1.0.0",
"description": "Tailwind Starter Template",
"license" : "MIT",
"repository": {
    "type" : "git",
    "url" : "https://github.com/tailwindtoolbox/StarterTemplate.git"
},
```

Refer to https://docs.npmjs.com/files/package.json for guidance

* Open your node command prompt/terminal and navigate to your 'project-name' folder and create the `node_modules` directory

   ```npm install or npm update```

* Refresh the Tailwind.js file

   ```npm run del:js && npm run create:js```

* Re-create the initial css file - (**######  Just run this after update tailwind.config.js ######**)

   ```npm run dev:css```

* Create purged and minified css / PurgeCSS - Remove "unused" css (Added by Sheeny Yang-2019-6-3)

   ```npm run build:css```

* Minify CSS / Cssnano - Remove "unused" css (Added by Sheeny Yang-2019-6-3)
   1.install:

   ```npm install cssnano --save-dev```
   ```npm install postcss-cli --global```

   2.run:

   ```postcss dist/css/tailwind.css > dist/css/tailwind.min.css```

* Start building your website using the starter template in the dist folder.

* Watch and output to directories by using folder paths:
  sass --watch <watch-path>:<output-path> (Added by Sheeny Yang-2019-6-5)

```sass --watch dist/scss:dist/css```


## Fix Tailwindcss (Added by Sheeny Yang-2019-7-3)
* delete below code //avoiding font size all the same as parent
h1,
h2,
h3,
h4,
h5,
h6 {
  font-size: inherit;
  font-weight: inherit;
}

blockquote,
dl,
dd,
h1,
h2,
h3,
h4,
h5,
h6,
figure,
p,
pre {
  margin: 0;
}

* modify below code //got problem below for uk-tab
*,
*::before,
*::after {
  border-width: 0;
  border-style: solid;
  border-color: #e2e8f0;
}

* change to below
*,
*::before,
*::after {
  border-width: 0;
  <!-- border-style: solid; -->
  border-color: #e2e8f0;
}


## Tweaking
* Customise the tailwind.config.js and tailwind.config.css to create the tailwind.css for your project
* Use purgecss/cssnano to remove unused CSS and minify the final CSS file

Refer to the [full setup guide for detailed instructions](https://www.tailwindtoolbox.com/setup)

## Bugs and Issues

Have a bug, suggestion or question? [Open a new issue](https://github.com/tailwindtoolbox/StarterTemplate/issues/new) here on GitHub.

## Creator

[Tailwind Toolbox](https://www.tailwindtoolbox.com/) was created by and is maintained by **[Amrit Nagi](https://amritnagi.info/)**, Co-owner of [Astrava.Solutions](https://astrava.solutions).

* https://twitter.com/tailwindtoolbox
* https://twitter.com/amritnagi
* https://github.com/tailwindtoolbox

Tailwind Toolbox is based on the [Tailwind CSS](https://www.tailwindcss.com/) framework created by [Adam Wathan](https://twitter.com/adamwathan), [Jonathan Reinink](https://twitter.com/reinink), [David Hemphill](https://twitter.com/davidhemphill) and [Steve Schoger](https://twitter.com/steveschoger)
