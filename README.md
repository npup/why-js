# Reproducing something I think is a problem (or at least a bug)

**Note**: This repo ships with a built `./dist` directory so you do not have to built it yourself if you don't want to.

To build this project yourself, do

    npm i
    npm run build

## Question

Why was `client.2ed951c6.js` generated in `./dist` directory for this project when built?  It is minified react- and react-dom related code.  
It seems to me it should not be there at all.

Of course, it is not referenced from any built page, but it seems like a mistake that it ends up in the built project anyway.


## Versions

This project, in its `package.json`, uses

    "devDependencies": {
        "astro": "^0.24.0",
        "prettier-plugin-astro": "^0.0.12"
    }

The problem (as I see it) is not observable in `astro@0.23.7` (see branch `version/0.23.7`).  No js is generated to `./dist` there.

