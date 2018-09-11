# Maven Multi module demo project


This project demo a way to create a multimodule project that is only outputting a single 
distrubution (jar).

## Project structure

```
├── dist  <------- the aggrigator module
│   ├── pom.xml
│   └── src
├── module1
│   ├── pom.xml
│   └── src
├── module2
│   ├── pom.xml
│   └── src
├── pom.xml
└── README.md
```

### Note:
- Only the dist module get deployed. 
- All modules get the same version as the parent pom version.
- Dependent modules module1 and module2 gets version dynamically updated.


## To build

- `mvn clean install`


## To release

- `mvn release:clean`
- `mvn release:prepare`
- `mvn release:perform`


