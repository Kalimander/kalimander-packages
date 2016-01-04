# kalimander-packages

###### Note: This project is still in early development and may not be complete for a while, but it may also be complete by tomorrow. Be patient.

This contains links to other github repositories for packages to install via Kalimander.
Each package should have its own file named by the following syntax:
`[package name].package`

Each line of the file should look like:

`[architecture] | [URL of repository at a specific version] | [version] | [install script within repository]`

*Optional:* One line (per architecture) should look like `[architecture] | [URL of github repository] | dev | [install script within repository]`

Accepted architectures must be the expected output of the command `uname -m` on compatible systems.
For example, if the target system produces `x86_64` as the output of `uname -m`, then the architecture would be either `x86_64`, a comma-separated list of compatible architectures including `x86_64`, or `all` if the program is compatible with every architecture.

The install script will be run at installation with the command `bash [script path]` where `script path` is the **relative path** once in the repository directory. Absolute paths will not be allowed. Root will not be implicitly given for install scripts. If root is required, either `sudo` must be used within the install script.
