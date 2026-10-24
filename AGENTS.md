# Repository workflow

Repository: `git@github.com:Oleksii1221/PDR_Test_APK.git`

Maintain these three branches:

- `dev` is the working branch for Android app development and documentation. Make normal commits here with short, descriptive English messages.
- `master` is for approved releases only. Do not commit to, merge into, or push `master` until the user explicitly says which `dev` commit is the release ("the latest `dev` commit" is sufficient). Every new release commit on `master` must have a message consisting only of the version, such as `v1.0.0` (`^v[0-9]+\.[0-9]+\.[0-9]+$`). Use the version requested by the user, or determine the next suitable version if none is given. Create a release snapshot whose tree matches the approved `dev` commit, with the previous `master` commit as its parent; this keeps development commit messages off `master`. After pushing that release, leave `master` untouched until the next explicit release instruction.
- `site` is for the project's website hosted on GitHub. Keep website work on this branch, separate from Android development. Use short, descriptive English commit messages.

Before Git operations, verify that the repository root is this `PDR_Test_APK` directory, since its parent directory also has a separate Git repository.
