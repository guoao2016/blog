[jsconfig](https://code.visualstudio.com/docs/languages/jsconfig)

```
{ 
  "compilerOptions": {
      "baseUrl": ".",
      "paths": {
        "@/*": ["./src/*"],
        "&/*": ["../mobile_mmp_public/*"],
        "#/*": ["../mobile_mmp_phone/src/*"]
      },
      "checkJs": false,
  },
  "exclude": ["node_modules", "../mobile_mmp_phone/node_modules"]
}

```
