# rootDir and outDir

If a bigger project, you don't want to just put all those `.js` file in the project. You want to have a more organized folder to store the compiled files. Now let's say you want to put the source files into the `src` folder and put the compiled files in the `dist` folder. So the project structure is as follows,

![](.gitbook/assets/image%20%287%29.png)

Then we can configure the `outDir` to specify where we store the file. Here it is `./dist` Now all the output files are placed in the `dist` folder. After that, just configuring the `index.html` to point it to the `dist/app.js` file.

![](.gitbook/assets/image%20%2812%29.png)

![](.gitbook/assets/image%20%289%29.png)

Now let's go to the `rootDir` attribute, specify it to `./src` will force typescript just look at the files from the src folder and don't look at other files.

Now let's say I by accidentally have some other `ts` files outside the `src` folder, configuring the `rootDir` will let typescript scan that and throw the error

![](.gitbook/assets/image%20%285%29.png)

