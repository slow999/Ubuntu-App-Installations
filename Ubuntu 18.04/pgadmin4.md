# pgAdmin4

### Dependencies
Python: 3.6


1. Go to https://www.postgresql.org/ftp/pgadmin/pgadmin4/v3.3/pip/ 
download pgadmin4-3.3-py2.py3-none-any.whl

2. Create a virtual env
Official document suggests installing pgadmin4 in virtual env. 
https://www.pgadmin.org/download/pgadmin-4-python-wheel/
``` shell
python3 -m virtualenv pgadmin4
```

3. Activate virtual env
``` shell
source pgadmin4/bin/activate
```

4. Install file
``` shell
pip install ./pgadmin4-1.3-py2.py3-none-any.whl
```

5. Run pgadmin4 in virtual env
``` shell
python3 pgadmin4/lib/python3.6/site-packages/pgadmin4/pgAdmin4.py
```

6. Create a shortcut script called 'pgadmin4'
``` shell
touch pgadmin4
chmod +x pgadmin4
nano pgadmin4
```
I personally would check 'Allow executing file as program' in file permissions tab.

Fill in code
``` shell
#!/bin/bash
cd ~/venv/pgadmin4
source bin/activate
python3 lib/python3.6/site-packages/pgadmin4/pgAdmin4.py
```

7. Run shortcut
Go to root folder where shortcut is
``` shell
./pgadmin4
```