# Effect Hook
## [BMI Calculator](https://sspbmical.ccbp.tech/)
- Persisting Application data
  - Local Storage
- Storing values in Local Storage
  - Using Effect Hook
- Tips for using Effect Hook
  - Multiple Effects
  - Dependency Array

## Persisting data while using React Hooks
### Storing values in Local Storage
- In useEffect we have access to the updated state values, so we write the logic for storing values inside it.\
- Once after getting the values from the Local Storage, provide them as the initial values for the useState hook.

## Tips for using the Effect Hook
Just like useState, you can also use multiple useEffects to separate unrelated logic into different effects based on what it is doing.

### Optimizing Performance by Skipping Effects
In some cases, executing the effect after every render creates a performance problem, It can be optimized by Skipping the effect when it is not required.\
The useEffect accepts another argument called ***Dependency Array***, using which we can control the execution of effect.
#### Syntax: `useEffect(effect, [var1, var2, ...])`
- The values we pass to the dependency array are called dependencies, which can be state variables or props.
- Effect will be executed whenever the dependencies are changed.
#### Without Dependencies
The Effect executes after every render.\
**`useEffect(effect)`**
#### Passing Empty Dependency Array
The Effect executes only once after the first render.\
`useEffect(effect, [])`
#### Passing Dependencies
The Effect executes when dependencies are changed.\
`useEffect(effect, [var1, var2,...])`




