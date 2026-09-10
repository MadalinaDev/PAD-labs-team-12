# Private service submodules

The directories here are Git submodules pointing to commits in individually owned private repositories. Their source and README files are stored in those repositories, not copied into this public repository.

Initialize only repositories you can access:

```sh
git submodule update --init services/battle-service services/tamagotchi-service
```

The professor(s) need invitations to each private repository to inspect a full recursive checkout. Teammates retain access only to their own private services; shared contracts remain in the [public README](../README.md).

See the [repository table](../README.md#repository-setup-and-lab-0-checklist) for the remaining service URLs and setup status.
