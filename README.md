# Database management system
[![Made with python](https://img.shields.io/badge/made%20with-python-color)
](https://www.python.org/)
[![Made with streamlit](https://img.shields.io/badge/made%20with-streamlit-red)](https://streamlit.io/)
[![Database](https://img.shields.io/badge/Database-mysql-blue)](https://www.mysql.com/downloads/)

## Note !
1. Please configure the database server information within the function 'connect' in database.py file.

2. Make sure you at least insert one teacher record (data) into table 老師, or you may encounter the error because of the foreign key constraint.

    <strong>For reference:</strong>
    This is my database table design.
    ```text
    老師 (老師id, 名字)
    論文 (論文id, 老師id(F.K.), 論文名稱, 共同合作者, 日期, 分類)
    學歷 (學歷id, 老師id(F.K.), 大學, 專業名, 學碩博)
    專長 (專長id, 老師id(F.k.), 專長描述)
    校內經歷 (校內經歷id, 老師id(F.K.), 校內任職地點, 校內職稱)
    校外經歷 (校外經歷id, 老師id(F.K.), 校外任職地點, 校外職稱)
    課表 (課程id, 老師id(F.K.), 課程名稱, 節次, 星期)
    ```

## Tech Stack
- mysql for database
- streamlit for web visualization
- python 
- pandas for data visualization
## Usage
1. Create virtual env.

```bash
# create env
python3 -m venv <env-name>

# activate env
# for mac user
source <env-name>/bin/activate 

# for windows user
.\<venv-name>\Scripts\activate\

```
2. Install all dependency after activate your environment.
```bash
    # In your environment
    pip install streamlit pandas pymysql pyperclip streamlit-option-menu

    # you can use 'pip list' to see the dependency install successfully or not.
    pip list
```

3. Run source code.
```bash
streamlit run 視覺化.py
```

