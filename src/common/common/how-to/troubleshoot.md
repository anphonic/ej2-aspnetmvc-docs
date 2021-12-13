# How to troubleshoot compile-time and run-time errors

## Compile-time error

* **Cannot find name 'Map' in `ej2.d.ts`: Need to change your target library. Try changing the 'lib' compiler option to `es2015` or later.**

    You may see the below error while running the application.

     > Error: **Build:Cannot find name 'Map'**. Do you need to change your target library? Try changing the 'lib' compiler option to `es2015` or later.

  **Cause:**

    This error is thrown due to not including the required target library for the TypeScript compiler option and it can be resolved by any one of the below solutions.

  **Solutions:**

    1. **Using MS build**

        By adding the required target `dom,es2015` library in `TypeScriptLib` MSBuild property in your `.csproj` file as like below, following the TypeScriptToolsVerison tag.

         ```csproj
            <TypeScriptToolsVersion>3.1</TypeScriptToolsVersion>
            <TypeScriptLib>dom,es2015</TypeScriptLib>
        ```

        > Note: If `tsconfig.json` exists in your project, the compiler will prioritize using the specified configuration options from `tsconfig.json` file. Otherwise, it’ll use the specified configuration options from the project file (`.csproj`).

        Refer [KB Link](https://www.syncfusion.com/kb/10136/typescript-library-upgrade-in-asp-net-mvc-project) for more details.

    2. **Using `tsconfig.json`**

        By adding the required target library in `"compilerOptions"` property as like below.

        ```json
        {
        "compilerOptions": {  
        //...  
        "target": "ES2015"  
        },  
        //...  
        }
        ```
