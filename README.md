# vscrazor-automobile

This project was build with [dotnet core](https://dotnet.microsoft.com/download/) version 2.2.1.

## Clone our app on git in Visual Studio Code

In terminal `git clone https://github.com/JosVermoesen/vscrazor-automobile.git` to get the codefiles on your computer.
Step into the directory `cd vscrazor-automobile` and do a `dotnet restore`

## Development server

Run `dotnet watch run` for a dev server. Navigate to `https://localhost:5001/`. The app will automatically reload if you change any of the code source files. For changes to the html razorpages refresh your browser

## Further help

To get more help on dotnet commands use `dotnet -h` or go check out the [dotnet documentation](https://docs.microsoft.com/nl-be/dotnet/).

## Fresh start in Visual Studio Code

Latest template:

- In terminal `dotnet new --install Microsoft.DotNet.Web.Spa.ProjectTemplates::2.2.1` to get the latest templates.
- In terminal `dotnet new -h` to list the available templates.

Fresh starting in terminal:

- **Make** directory `md vscrazor-automobile`
- **cd** into that directory `cd vscrazor-automobile`
- **generate** the new webapp project with template `dotnet new webapp --auth Individual` for Webapp with razor pages and identity with sql lite database.
- add **package reference** for preparing all identity code `dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design` followed by `dotnet restore`
- for adding **all identity** functions `dotnet aspnet-codegenerator identity -dc vscrazor_automobile.Data.ApplicationDbContext`
- **remove** the sqllite database and migrations folder
- start a **clean db** with full identity functionality `dotnet ef migrations add InitDbWithFullIdentity` and refresh the new db `dotnet ef database update`
