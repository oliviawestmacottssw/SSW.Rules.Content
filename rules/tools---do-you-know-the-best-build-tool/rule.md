---
type: rule
title: Tools - Do you know the best Build Tool?
uri: tools---do-you-know-the-best-build-tool
created: 2016-08-02T14:15:28.0000000Z
authors:
- id: 24
  title: Adam Stephensen
- id: 34
  title: Brendan Richards

---

Building, bundling and compiling Angular applications can get complicated. You need great build tools.
  
[[badExample]]
| ![Gulp requires hundreds of lines of config to build and bundle Angular applications](gulp.png)
 
[[goodExample]]
| ![Webpack is an open-source JavaScript module bundler that can be used to build your application](webpack.png)(and lots more as well). Teams with advanced build requirements use Webpack. The downside of Webpack is that it requires a large investment in learning Webpack - if it isn't required, the Angular CLI is a better choice 
[[goodExample]]
| ![Use the Angular CLI on all new projects that don't require custom Webpack builds. The Angular CLI generates components, routes, services, and pipes, follows best practices as well as building applications for production. The Angular CLI build includes best practices including Tree Shaking and Ahead of Time](cli.png)(AoT) compilation out of the box! The Angular CLI uses Webpack under the covers
