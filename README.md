# Remote SSH Commands

Simple GitHub Action to run a command on a remote server using SSH. This is working with the latest [GitHub Actions](https://github.com/features/actions).


## ✨ Example Usage

**Example using OpenSSH private key**

```yml
- name: ls -a via ssh
  uses: tarunjangra/ssh-action@master
  with:
    command: |
      cd /tmp
      ls -a
    host: ${{ secrets.HOST }}
    user: root
    key: ${{ secrets.PRIVATE_KEY}}
```

## Options

- **host** - _string_ - Hostname or IP address of the server. **Default:** `'localhost'`

- **port** - _integer_ - Port number of the server. **Default:** `22`

- **user** - _string_ - Username for authentication. **Default:** (root)

- **key** - _string_ - Required, that contains a private key for either key-based or hostbased user authentication (OpenSSH format). **Default:** (none)

- **pass** - _string_ - Password for authentication. 

- **args** - _string_ - SSH parameters for example: -tt.

> Password and Private Key can only be configured one item