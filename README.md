# Ops utilities toolbelt for novostack.

`Dependencies`
  - [jq](https://jqlang.github.io/jq/download/) - JQ is used to parse the configurations for Node.JS. This stack is currently on Node.JS so other parsers are not supported.


## Scripts

`status` - Provides a way to check if a service is running. Takes service name as the argument and expects the local path to match it. Uses `lsof` to identify a listening process at a port provided by the service configs.

`restart` - Provides a way to start one/all services based on the above status checker.

`checkGIT` - Provides a minimal report on status of the local service repository.

`checkRemote` - Provides a minimal report of the local service repository against remote.

`update` - Updates service dependencies.


`updateUtils` - Provides an interface to update services with the latest version of [`novostack-utils`](https://github.com/techiev2/novostack-utils) and adds the latest remote version as dependency
  - TODO: Update the script to allow version bumps via releases.
  
`switchToLocalUtils` - Allows services to switch to a local version of `novostack-utils`.


`resetUtils` - Resets local usage of `novostack-utils` and reintroduces remote packages.