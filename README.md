# tiny-git-service

Very small git-over-ssh service with per-user permissions. This is a work in progres.

## Installation

In `/etc/ssh/sshd_config`, add these options:

    AuthorizedKeysCommandUser nobody
    
    Match User git
        AuthorizedKeysCommand /opt/hotplate/git/restricted-shell find-key %f

Adjusting the paths as necessary. The script also has some paths near the top which will need to be adjusted.
