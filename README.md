# Introduction

`Hot Reload` feature has been introduced in `Visual Studio 2022` recently. In this way you can `Edit` your codes while your project is running. However you can still use this feature in the `Visual Studio 2019` and older versions in a way. In this page I am going to tell you how.

# How to use

* In order to enable `Hot Reload` or `Edit and Continue` feature in `Visual Studio` you need to add `Razor RuntimeCompilation` to your project. Use the command below to add via `Nuget`:

```Nuget
  Install-Package Microsoft.AspNetCore.Mvc.Razor.RuntimeCompilation
```
* Add the code below in your `Startup.cs` class:
```C#
  public void ConfigureServices(IServiceCollection services)
  {
      services.AddControllersWithViews();
      services.AddRazorPages().AddRazorRuntimeCompilation();

  }
```

