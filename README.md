# PackageFactory.AtomicFusion.ClassNames

> ÈEl Helper for rendering of classNames in atomic fusion

### EEL-Helpers

- `AtomicFusion.classNames`: render all arguments as classNames and apply conditions if needed

All arguments of the AtomicFusion.classNames eelHelper are evaluated 
and the following rules are applied

- falsy values: (null, '', [], {}) are not rendererd
- array: all items that are scalar and truthy are rendered as class-name
- object: keys that have a truthy values are rendered as class-name
- scalar: is cast to string and rendered as class-name
        
## Usage 

### 1. Component definition

```
prototype(Vendor.Site:Component) < prototype(Neos.Fusion:Component) {
    renderer = afx`
        <div class={AtomicFusion.classNames('component' , {'component--bold': props.bold})}>
            {props.content}
        </div>
    `
}
```

## Installation

PackageFactory.AtomicFusion is available via packagist. Just run `composer require packagefactory/atomicfusion-classnames`. 

We use semantic-versioning so every breaking change will increase the major-version number.

## License

see [LICENSE file](LICENSE)
