# Including & Excluding Files

Add `"exclude": ["analytics.ts"]` in the `tsconfig.json`, we can exclude the files in the array to be compiled. Some typical use cases are those "dev" files, like

* `"app.dev.ts"`
* `"*.dev.ts"`
* `"**/*.dev.ts"`
* `"node_modules"` //_this would be default, if you don't add this, this will be excluded automatically_

![](../.gitbook/assets/image%20%288%29.png)

`include` will be the opposite, but the total will be the `include` minus the `exclude`

`files` will be the list of the files you want to include, just good for small projects

