# Versatia examples

Every example is a repository of its own: one Paper 1.21.4 plugin (two, where the feature is about
two plugins) showing exactly one feature of the [Versatia framework](https://versatiaframework.github.io/VersatiaDocs/), with one file to
read, the log lines to expect and a few things to try. Repositories are named
`VersatiaExample-<Topic>-<Feature>`, so they sort by topic on GitHub; the order in which to read
them is below.

## Before you start

Every example runs on a Paper 1.21.4 server with VersatiaCore installed. The examples whose
"Things to try" reload a plugin with `/versatia reload` also need the
[CommandAPI](https://commandapi.jorel.dev) 12.x plugin, which registers that command; each README
lists what its example needs under Building.

## Learning path

1. [VersatiaExample-Resources-Extraction](https://github.com/VersatiaFramework/VersatiaExample-Resources-Extraction): Shows how files under `resources/` are extracted into the data folder
2. [VersatiaExample-DI-Beans](https://github.com/VersatiaFramework/VersatiaExample-DI-Beans): Shows local beans, constructor injection and the injected `Logger` every plugin has
3. [VersatiaExample-DI-Qualifiers](https://github.com/VersatiaFramework/VersatiaExample-DI-Qualifiers): Shows `@Qualifier` and `@Primary` resolving several beans of one type
4. [VersatiaExample-DI-CustomScope](https://github.com/VersatiaFramework/VersatiaExample-DI-CustomScope): Shows a plugin-defined scope annotation inheriting a built-in one
5. [VersatiaExample-DI-PrivateBeans](https://github.com/VersatiaFramework/VersatiaExample-DI-PrivateBeans): Shows private beans and functions handled through reflection
6. [VersatiaExample-Lifecycle-AutoInvoke](https://github.com/VersatiaFramework/VersatiaExample-Lifecycle-AutoInvoke): Shows `@AutoInvoke` on the main class, a bean and an object
7. [VersatiaExample-Config-Values](https://github.com/VersatiaFramework/VersatiaExample-Config-Values): Shows `@Value` properties set from YAML files at start and reload
8. [VersatiaExample-Lifecycle-Reload](https://github.com/VersatiaFramework/VersatiaExample-Lifecycle-Reload): Shows a plugin designed for reload: values re-read, a derived value rebuilt, a task rescheduled when its interval changes
9. [VersatiaExample-Events-Listeners](https://github.com/VersatiaFramework/VersatiaExample-Events-Listeners): Shows Bukkit listeners registered automatically, with injection
10. [VersatiaExample-Tasks-Background](https://github.com/VersatiaFramework/VersatiaExample-Tasks-Background): Shows a `BackgroundTask` broadcasting at a configured period, restarted by every reload
11. [VersatiaExample-Tasks-PluginScope](https://github.com/VersatiaFramework/VersatiaExample-Tasks-PluginScope): Shows coroutines of your own in the injected `PluginScope`: a combat tag per player in `KeyedJobs`
12. [VersatiaExample-Tasks-Conditions](https://github.com/VersatiaFramework/VersatiaExample-Tasks-Conditions): Shows conditions rechecked on events: a teleport countdown cancelled by moving, a beacon lit while players are online
13. [VersatiaExample-Tasks-Threads](https://github.com/VersatiaFramework/VersatiaExample-Tasks-Threads): Shows file reading moved off the server thread with `withContext(Dispatchers.IO)` and back for the Bukkit calls
14. [VersatiaExample-DI-OptionalPlugins](https://github.com/VersatiaFramework/VersatiaExample-DI-OptionalPlugins): Shows a bean conditional on Vault with a fallback, and a condition of your own
15. [VersatiaExample-DI-SharedBeans](https://github.com/VersatiaFramework/VersatiaExample-DI-SharedBeans): Shows beans exposed by one plugin and injected by another
16. [VersatiaExample-Enhancements-FeatureSwitches](https://github.com/VersatiaFramework/VersatiaExample-Enhancements-FeatureSwitches): Shows `@DisableVersatiaFeatures` on a base class and on the main class
17. [VersatiaExample-Enhancements-Custom](https://github.com/VersatiaFramework/VersatiaExample-Enhancements-Custom): Shows a custom enhancement: an annotation and its processor in a library plugin
18. [VersatiaExample-Modules-Messages](https://github.com/VersatiaFramework/VersatiaExample-Modules-Messages): Shows the Messages module: files under `messages/` reloaded with the plugin, filled with runtime arguments

## By topic

### Resources

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-Resources-Extraction](https://github.com/VersatiaFramework/VersatiaExample-Resources-Extraction) | How files under `resources/` are extracted into the data folder | [Plugin resources](https://versatiaframework.github.io/VersatiaDocs/docs/resources) |

### Configuration

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-Config-Values](https://github.com/VersatiaFramework/VersatiaExample-Config-Values) | `@Value` properties set from YAML files at start and reload | [Configuration values](https://versatiaframework.github.io/VersatiaDocs/docs/configuration) |

### Dependency injection

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-DI-Beans](https://github.com/VersatiaFramework/VersatiaExample-DI-Beans) | Local beans, constructor injection and the injected `Logger` every plugin has | [Dependency injection](https://versatiaframework.github.io/VersatiaDocs/docs/dependency-injection) |
| [VersatiaExample-DI-Qualifiers](https://github.com/VersatiaFramework/VersatiaExample-DI-Qualifiers) | `@Qualifier` and `@Primary` resolving several beans of one type | [Names, qualifiers and `@Primary`](https://versatiaframework.github.io/VersatiaDocs/docs/dependency-injection/qualifiers) |
| [VersatiaExample-DI-CustomScope](https://github.com/VersatiaFramework/VersatiaExample-DI-CustomScope) | A plugin-defined scope annotation inheriting a built-in one | [Defining your own scope](https://versatiaframework.github.io/VersatiaDocs/docs/internals/enhancements#defining-your-own-scope) |
| [VersatiaExample-DI-PrivateBeans](https://github.com/VersatiaFramework/VersatiaExample-DI-PrivateBeans) | Private beans and functions handled through reflection | [Direct access versus reflection](https://versatiaframework.github.io/VersatiaDocs/docs/internals/descriptor#direct-access-versus-reflection) |
| [VersatiaExample-DI-SharedBeans](https://github.com/VersatiaFramework/VersatiaExample-DI-SharedBeans) | Beans exposed by one plugin and injected by another | [Beans across plugins](https://versatiaframework.github.io/VersatiaDocs/docs/dependency-injection/cross-plugin) |
| [VersatiaExample-DI-OptionalPlugins](https://github.com/VersatiaFramework/VersatiaExample-DI-OptionalPlugins) | A bean conditional on Vault with `@Primary`, a fallback without it, and a condition of your own | [Optional plugins](https://versatiaframework.github.io/VersatiaDocs/docs/optional-plugins) |

### Lifecycle

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-Lifecycle-AutoInvoke](https://github.com/VersatiaFramework/VersatiaExample-Lifecycle-AutoInvoke) | `@AutoInvoke` on the main class, a bean and an object | [Auto-invoked functions](https://versatiaframework.github.io/VersatiaDocs/docs/lifecycle/auto-invoke) |
| [VersatiaExample-Lifecycle-Reload](https://github.com/VersatiaFramework/VersatiaExample-Lifecycle-Reload) | A plugin designed for reload: values re-read, a derived value rebuilt, a task rescheduled when its interval changes, a reload from code | [Reloading plugins](https://versatiaframework.github.io/VersatiaDocs/docs/lifecycle/reload) |

### Events

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-Events-Listeners](https://github.com/VersatiaFramework/VersatiaExample-Events-Listeners) | Bukkit listeners registered automatically, with injection | [Event listeners](https://versatiaframework.github.io/VersatiaDocs/docs/events) |

### Tasks

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-Tasks-Background](https://github.com/VersatiaFramework/VersatiaExample-Tasks-Background) | A `BackgroundTask` broadcasting at a configured period, restarted by every reload | [Background tasks](https://versatiaframework.github.io/VersatiaDocs/docs/tasks#background-tasks) |
| [VersatiaExample-Tasks-PluginScope](https://github.com/VersatiaFramework/VersatiaExample-Tasks-PluginScope) | Coroutines of your own in the injected `PluginScope`: a combat tag per player in `KeyedJobs` | [Your own coroutines](https://versatiaframework.github.io/VersatiaDocs/docs/tasks#your-own-coroutines) |
| [VersatiaExample-Tasks-Conditions](https://github.com/VersatiaFramework/VersatiaExample-Tasks-Conditions) | Conditions rechecked on events: a teleport countdown cancelled by moving, a beacon lit while players are online | [Conditions](https://versatiaframework.github.io/VersatiaDocs/docs/tasks#conditions) |
| [VersatiaExample-Tasks-Threads](https://github.com/VersatiaFramework/VersatiaExample-Tasks-Threads) | File reading moved off the server thread with `withContext(Dispatchers.IO)` and back for the Bukkit calls | [Threads](https://versatiaframework.github.io/VersatiaDocs/docs/tasks#threads) |

### Enhancements

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-Enhancements-FeatureSwitches](https://github.com/VersatiaFramework/VersatiaExample-Enhancements-FeatureSwitches) | `@DisableVersatiaFeatures` on a base class and on the main class | [Enhancements on a base class](https://versatiaframework.github.io/VersatiaDocs/docs/internals/enhancements#enhancements-on-a-base-class) |
| [VersatiaExample-Enhancements-Custom](https://github.com/VersatiaFramework/VersatiaExample-Enhancements-Custom) | A custom enhancement: an annotation and its processor in a library plugin | [Defining your own enhancement](https://versatiaframework.github.io/VersatiaDocs/docs/internals/enhancements#defining-your-own-enhancement) |

### Modules

| Example | Shows | Documentation |
|---|---|---|
| [VersatiaExample-Modules-Messages](https://github.com/VersatiaFramework/VersatiaExample-Modules-Messages) | The Messages module: files under `messages/` reloaded with the plugin, filled with runtime arguments | [Messages module](https://versatiaframework.github.io/VersatiaDocs/docs/modules/messages) |

## Adding an example

Start from [VersatiaExample-Template](https://github.com/VersatiaFramework/VersatiaExample-Template) ("Use this template"),
keep the README sections, add an entry to the learning path and a row to its topic table above, and
an example card to the documentation page the example illustrates.
