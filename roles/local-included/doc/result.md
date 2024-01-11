```bash
$ ansible-playbook -i inventories/local/host.ini local-included.yml -C

PLAY [included test] **********************************************************************************************************************************************

TASK [local-included : Include variables from users.test] *********************************************************************************************************
ok: [mypc]

TASK [local-included : Debug information] *************************************************************************************************************************
ok: [mypc] => {
    "users": [
        {
            "age": 33,
            "key": "marioaaaaaa",
            "name": "char"
        },
        {
            "age": 42,
            "key": "mariobbbbbb",
            "name": "str"
        }
    ]
}

PLAY RECAP ********************************************************************************************************************************************************
mypc                       : ok=2    changed=0    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
```