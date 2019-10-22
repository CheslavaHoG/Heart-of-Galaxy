# Heart-of-Galaxy

This repository is dedicated to the development of Heart of Galaxy. 

## Rules of Engagement

The following rules are meant to keep the quality of the code as high as possible by having a single standard to follow. The idea behind these rules is only in part personal taste. The other reasons are clearly to make it as easy as possible for others to jump in the project and to allow a future conversion to Java (or another language different from JavaScript).

### 1. Code style

- CamelCase java style always. It means UpperCamelCase for class names, lowerCamelCase for variables and methods.
- **No underscores**. They are forbidden.
- Use hyphens "-" and lower case for HTML/CSS.
- Use " always in javascript. Use ' always in HTML/CSS (as well as embedded html/css in javascript code).

### 2. Project structure

#### Number of files

Having too many files is unnecessary overhead. Having one big file is even worse. The idea is to think twice before introducing a new file. The structure of the project should follow more or less what is defined in the next sections.

#### Folders

Each folder should be roughly the equivalent of a Java component/module. Nested folders are ok, as long as the depth of the folders hierarchy is contained. Think of the penalty associated with the depth N as a function N^N. 1 is perfect, 2 is ok, 3 is already too much. If the first level is reserved to components and the second level to modules, we don't really need any more nesting.

One special folder will be reserved for testing.

ROOT
|- Component1
  |- API
  |- Implementation
|- Component2
  |- API
  |- Implementation
|- ...
  |- ...
|- Tests
  |- Component #1 test
  

#### Files

Each file should be roughly the equivalent of a Java package. Ideally each component should have a well defined API and a well defined implementation. Two files/folders should be sufficient. Ideally, the API will contain only interfaces but this is a bit difficult to achieve with vanilla javascript. In this case, interface means façade to the underlying system.

### 3. Incapsulation

As hard as it can be with Javascript to hide implementation details, incapsulation should be the way to go. Getter and setters are required for every variable.

### Object creation

Generally constructors will be fine as long as they accept only one parameter. The one parameter will contain key-values entries to initialize internal variables. Keep the number of entries as small as possible. Builders are also fine 

### 4. Dependencies

Avoid at all costs external dependencies. Everything is possible with vanilla javascript. The only exception is for the GUI (and maybe in the future for server side). It would be nice to introduce ONE of the followings:

- Angular
- React

### 5. Type safety

This is an open question. How to do it or at least to make sure that the impact of not having type safety would be as small as possible?

- External dependencies for type checks: I don't believe it will be a neat solution.
- 

### 6. Testing

Unit test every new bit of logic added
