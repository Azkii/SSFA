## Project Structure

Most of the code lives in the `src` folder and looks something like this:

```sh
/app               # application layer containing:
    .../routes        # application routes
    .../app.tsx       # main application component
    .../app-provider  # application provider that wraps the entire application with global providers.
/assets            # assets folder can contain all the static files such as images, fonts, etc.
/components        # shared components used across the entire application
/config            # global configurations, exported env variables etc.
/features          # feature based modules
/hooks             # shared hooks used across the entire application
/lib               # reusable libraries preconfigured for the application
/stores            # global state stores
/test              # test utilities and mocks
/types             # shared types used across the application
/utils             # shared utility functions
/mocks             # API calls mocks
```

## Feature structure

For easy scalability and maintenance, organize most of the code within the features folder. Each feature folder should contain code specific to that feature, keeping things neatly separated. This approach helps prevent mixing feature-related code with shared components, making it simpler to manage and maintain the codebase compared to having many files in a flat folder structure.

<span style="color: gray; font-style: italic;">
    NOTE: You don't need all of these folders for every feature. Only include the ones that are necessary for the feature.
    </br></br>
</span>

```sh
/features/awesome-feature # feature directory
    .../api         # exported API request declarations and api hooks related to a specific feature
    .../assets      # assets folder can contain all the static files for a specific feature
    .../components  # components scoped to a specific feature
    .../hooks       # hooks scoped to a specific feature
    .../stores      # state stores for a specific feature
    .../types       # typescript types used within the feature
    .../utils       # utility functions for a specific feature
```
