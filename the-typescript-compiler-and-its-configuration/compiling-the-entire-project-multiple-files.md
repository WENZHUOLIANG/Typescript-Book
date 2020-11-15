# Compiling the Entire Project / Multiple Files

If you have more than one files in the project. Let's say we have the `analytics.ts` in the project.

![](../.gitbook/assets/image%20%289%29.png)

Firstly run the `tsc --init` command, this command will specify that the project is managed by typescript. And this command will generate the `tsconfig.json` file. This basically is the indicator for typescript back project in which this file lies and all sub folders of this folder should be managed by typescript. 

Now if we run the `tsc` command, all the files will be compiled with the `js` file.

