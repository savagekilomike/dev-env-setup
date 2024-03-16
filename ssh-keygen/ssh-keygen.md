from EPAM Data Engineering
```bash
ssh-keygen -t rsa -C "name@domain"
```

`ssh-keygen` is a tool for generating new authentication key pairs for SSH (Secure Shell). It's a useful utility for creating keys that allow you to authenticate to servers and services securely without needing to use passwords. Here's a basic guide on how to use `ssh-keygen`:

### 1. Open a Terminal

First, you need to open your terminal or command prompt.

### 2. Generate a New SSH Key Pair

To generate a new SSH key pair (which includes a private key and a public key), simply type the following command:

```bash
ssh-keygen
```

By default, this will create a 2048-bit RSA key pair. You can specify a different type and size of key with additional options. For example, to create a more secure 4096-bit RSA key, use:

```bash
ssh-keygen -t rsa -b 4096
```

### 3. Specify the File to Save the Key

After running the `ssh-keygen` command, you'll be asked where to save the new key. By default, this is in the `.ssh` directory in your home folder (`~/.ssh/id_rsa` for RSA keys). You can press Enter to accept the default or specify a different path.

If you already have a key in the default location and you don't want to overwrite it, you should specify a new filename.

### 4. Enter a Passphrase (Optional)

Next, you'll be asked to enter a passphrase. A passphrase adds an additional layer of security by encrypting the private key on disk with the passphrase. If you don't want to use a passphrase, just press Enter (though it's recommended to use one for enhanced security).

### 5. Public and Private Keys

After you've completed the steps, `ssh-keygen` will generate your SSH key pair. The private key will be saved to the specified file (e.g., `~/.ssh/id_rsa`), and the public key will be saved to a file with the same name but with `.pub` appended (e.g., `~/.ssh/id_rsa.pub`). The private key should be kept secure and private, while the public key can be shared.

### 6. Copy the Public Key to Your Server

To use your new SSH key, you'll need to copy the public key to the server you want to connect to. The easiest way to do this is with the `ssh-copy-id` utility (if available on your system):

```bash
ssh-copy-id user@hostname
```

Replace `user@hostname` with your actual username and the hostname or IP address of the server.

If `ssh-copy-id` isn't available, you can manually add your public key to the `~/.ssh/authorized_keys` file on the server.

### Additional Options

- **Key Types**: Besides RSA, you can generate keys of types DSA, ECDSA, or ED25519 by using the `-t` option, e.g., `-t ed25519`. ED25519 is recommended for most users due to its balance of security and performance.
- **Customizing File Name**: Use `-f` to specify a custom path and filename for your keys.

Remember, the private key should never be shared with anyone. You distribute your public key to systems where you need to authenticate.