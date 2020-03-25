# ember-engines-router-service
==============================================================================

Provides the [Router service](https://api.emberjs.com/ember/release/classes/RouterService) for ember-engines.


## Compatibility
------------------------------------------------------------------------------

* Ember.js v3.12 or above
* Ember CLI v2.13 or above
* Node.js v10 or above


## Installation
------------------------------------------------------------------------------

```
ember install ember-engines-router-service
```


## Usage

Basically you have all [RouterService](https://api.emberjs.com/ember/release/classes/RouterService) API with `*External` sufix to each one using new "external routing" APIs such as `transitionToExternal` and `isActiveExternal`.

------------------------------------------------------------------------------
```js
import Component from '@glimmer/component';
import { inject as service } from '@ember/service';
import { action } from "@ember/object";

export default class SomeComponent extends Component {
  @service router;

  @action
  transitionToHome() {
    this.router.transitionToExternal('other.route');
  }

  @action
  redirectToHome() {
    this.router.replaceWithExternal('other.route');
  }
}
```

For further documentation on this subject, view the [Engine Linking RFC](https://github.com/emberjs/rfcs/pull/122).


## Contributing
------------------------------------------------------------------------------

See the [Contributing](CONTRIBUTING.md) guide for details.


## License
------------------------------------------------------------------------------

This project is licensed under the [MIT License](LICENSE.md).
