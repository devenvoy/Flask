### create new Virtual env

1. install virtualenv package 
```sh
pip3 install virtualenv 
# or
brew install virtualenv
```

2. create new virtual envrionment 
``` sh
virtualenv <env_name>
```

3. start or invoke env 
```sh
source <env_name>/bin/activate
```


### start learning flask
- add flask module in env
```python
pip3 install flask
```
- add flask_sqlalchemy for dtabase operation 
```python
pip3 install flask_sqlalchemy 
```


1. create server using flask
    - create app.py file
    - look at app.fy from this project 
    - create application by using `Flask(__name__)`
    - add app configuration in `app.config[]` array
    - create database using `SQLAlchemy(app)`
    - define database schema by create Model class or POJO class 
    
2. add pages for your website 
    - add two folder in your project 
        a) `static`
        b) `templates`
    - add all web page in templates folder otherwise it will not be found on runtime 
    - add all css and js file in static folder
    - create methods for each webpages 
    - this method will return compile web pages using 
    `render_template('page_file_name')`
    - to define navigation annotate this method using `@app.route('path')`

3. invoke database from teminal
    - go to termianl
    - start pyhton shell by command `python3`
    - execute following command 
    ```python
    from app import app , db
    app.app_context().push()
    db.create_all()
    exit()
    ```
    - close terminal


4. Run App 
    - add this code to start running app 
    ```
    if __name__ == "__main__":
    app.run(debug=True)
    ```