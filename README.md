# Portal QA Automation Engineer assignment

Hi!

We would like to understand your approach to writing automated tests, so that's why we ask you to do this assignment. 

We will evaluate your code on structuring, readability and maintanability. During the interview we will have a short talk about your code too.

## Objective

### Introduction

Please write a test automation using PlayWright for a demo application. It is up to you to use either C# or TypeScript.

> This demo application is a modified version of the Blazor with Local Identity demo. The original can be found here:   [Secure ASP.NET Core Blazor WebAssembly with ASP.NET Core Identity](https://learn.microsoft.com/aspnet/core/blazor/security/webassembly/standalone-with-identity).


### Requirements
 - Cover at least 3 scenarios.
   - It is (almost, see below) up to you which scenarios to cover.
 - At least one scenario should test the [data processing](http://localhost:5170/data-processing) form.
   - The data processing form returns the lenght of the input provided.
   - This form only works when the user is authenticated. See [authentication](#authentication) for the standard logins.
 
 - It is up to you to decide on the other scenarios.
   - Note that you can test for example both positive and negative paths.

### Deliverable

Please send us back the complete source code, preferrably as a Git repository. You could send us a zipped archive or invite us to a private GitHub repository. Sharing your solution publicly on the internet will disqualify your submission. Please include this Readme.md file in your submission.

Last but not least, we should be able to compile and run your tests.

## Steps to run the demo

1. Run the demo application by using the included [`docker-compose`](compose.yaml)  file
    1. Docker needs to be installed on your system.
    1. From the root of the project, run `docker-compose up`
    1. You can browse the application at [http://localhost:5170](http://localhost:5170)

### Authentication

Whenever an user is authenticated, some more functionality becomes available. 

* `admin@greenflux.com` (Password: `Passw0rd!`). Admin has `Administrator`, `Manager`, and `User` roles and can access the private manager page but not the private editor page of the app. She can process data with both forms on the data processing page.
* `user@greenflux.com` (Password: `Passw0rd!`). This user only has the `User` role and can't access the manager and editor pages. He can only process data with the first form on the data processing page.

