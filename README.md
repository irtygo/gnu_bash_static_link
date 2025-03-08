Introduction
============

This repository provides precompiled, statically linked builds of **GNU Bash 4.4** for **x86_64** and **x86_32** architectures, built using GitHub Actions.

The source code is identical to the official GNU Bash 4.4, with the only difference being that the binaries are statically linked. You can download the latest precompiled binaries from the [Releases page](https://github.com/irtygo/gnu_bash_static_lin/releases/latest), or access them from the artifacts of the GitHub Actions workflow.

For the official **GNU Bash** project, please visit the upstream repository: [gitGNU/gnu_bash](https://github.com/gitGNU/gnu_bash).

To compile Bash from source (with static linking):

1. Clone the repository:
    ```bash
    git clone https://github.com/irtygo/gnu_bash_static_lin.git
    ```

2. Enter the directory:
    ```bash
    cd gnu_bash_static_lin
    ```

3. Configure the build with static linking:
    ```bash
    ./configure LDFLAGS="-static"
    ```

    - **`LDFLAGS="-static"`**: This flag ensures that the binary is statically linked, meaning all dependencies will be included in the final executable, rather than relying on shared libraries at runtime.

4. Build Bash:
    ```bash
    make -j$(nproc)
    ```

5. (Optional) Install Bash on your system:
    ```bash
    sudo make install
    ```

This will build and install a statically linked version of Bash. The only difference from the official Bash is that these binaries are statically linked. If you need to modify the build process further, refer to the upstream repository for guidance on customizations.

Reporting Bugs
==============
Bug reports for Bash should be sent to:

    bug-bash@gnu.org

You can also report issues via the GitHub repository's Issues page, where bugs and feature requests are discussed.

Enjoy using **GNU Bash**!
