# ansible-29-lint

Linter for Ansible 2.9.x. based on PyPi [ansible-lint@5.4.0](https://pypi.org/project/ansible-lint/5.4.0/) (last versions with
2.9.x support).

Unfortunately, modern system runs python > 3.10, so the ansible 2.9.x packages
are not compatible with that. To run, after installed the package from Mason,
go to:

    $ cd ~/.local/share/nvim/mason/packages/ansible-29-lint

Directory, remove (or move) the generated venv, then from a python3.9 executable
(you can install it with brew on macOS or your distro package manager), generate
a new one:

    $ python3.9 -m venv venv

then create a new requirements.txt package with this list inside:

    ansible==2.9.13
    ansible-lint==5.4.0
    bracex==2.4
    cffi==1.16.0
    cryptography==43.0.0
    enrich==1.2.7
    Jinja2==2.10.1
    jinja2-ansible-filters==1.3.0
    markdown-it-py==3.0.0
    MarkupSafe==0.23
    mdurl==0.1.2
    packaging==24.1
    pip==24.0
    pycparser==2.22
    Pygments==2.18.0
    PyYAML==6.0.1
    rich==13.7.1
    ruamel.yaml==0.18.6
    ruamel.yaml.clib==0.2.8
    tenacity==8.5.0
    wcmatch==8.5.2

Finally, install these packages:

    $ source venv/bin/activate
    (venv) $ pip install -r requirements.txt
    ...

Then check ansible and ansible-lint version:

    (venv) $ ansible --version
    ansible 2.9.13
    ...
    
    (venv) $ ansible-lint --version
    ansible-lint 5.4.0 using ansible 2.9.13
