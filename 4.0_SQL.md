## Content

1. What is SQL?
   - Types of SQL Statements
      - Data Definition Language (DDL)
      - Data Manipulation Language (DML)
      - Data Control Language (DCL)
      - Transaction Control Language (TCL)
   - SQL Constraints
   - SQL Relationships
      - One-to-One
      - One-to-Many
      - Many-to-Many

---

### 1. What is SQL?

   SQL ဆိုတာ Structured Query Language ရဲ့ အတိုကောက်ဖြစ်ပြီး, Relational Database Management Systems (RDBMS) တွေမှာ Data တွေကို Access, Manage, Control လုပ်ဖို့ အဓိကအသုံးပြုတဲ့ Language ပါ။

   SQL မှာ RDBMS ထဲက Data တွေကို Create, Read, Update, Delete လုပ်နိုင်ပါတယ်။ SQL Language ကို IBM က 1970s ကထဲက စတင်ဖန်တီးခဲ့ပြီး, အခုဆိုရင် SQL ကို Oracle, MySQL, SQL Server, PostgreSQL စတဲ့ RDBMS တွေမှာ အသုံးပြုကြပါတယ်။

   SQL Language ကို အသုံးပြုရာမှာ Basic အချက်အလက်တွေအနေနဲ့ Schema, Table, Row, Column တွေကို သိဖို့လိုပါတယ်။ Schema က Database Structure ကို ကိုယ်စားပြုပြီး, Table တွေက Schema ထဲမှာရှိတဲ့ Data Set Collection တွေကို သိမ်းဆည်းထားတဲ့ စနစ်ပါ။ Row တစ်ခုက Record တစ်ခုကို ကိုယ်စားပြုပြီး, Column တစ်ခုက Data Field တစ်ခုကို ကိုယ်စားပြုပါတယ်။

#### Types of SQL Statements

   SQL Commands တွေကို Data Handling ပုံစံအလိုက် အောက်မှာဖော်ပြထားတဲ့ (၄) မျိုးခွဲထားပါတယ်။

   #### 1. Data Definition Language (DDL)

   DDL Commands တွေက Database Schema နဲ့ အလုပ်လုပ်ပါတယ်။ Table, Index, View စတာတွေကို Create, Alter, Drop လုပ်ပါတယ်။

   - **Common DDL Commands:**
      - **CREATE** – Table, Database, Index, View တို့ကို Create လုပ်ပါတယ်။
      - **ALTER** – Existing Table Structure ကို ပြောင်းလဲနိုင်ပါတယ်။
      - **DROP** – Table, Database, Index, View တို့ကို ဖျက်နိုင်ပါတယ်။

      ```sql
      CREATE TABLE Customers (
         ID INT PRIMARY KEY,
         Name VARCHAR(50),
         Age INT
      );
      ```

   #### 2. Data Manipulation Language (DML)

   DML Commands တွေက Database ထဲမှာရှိတဲ့ Data တွေကို Manipulate လုပ်ဖို့အတွက် အသုံးပြုပါတယ်။

   - **Common DML Commands:**
      - **SELECT** – Database ထဲက Data တွေကို Select လုပ်တယ်။
      - **INSERT** – Table ထဲကို Data အကုန်သွင်းတယ်။
      - **UPDATE** – Table ထဲက Data ကို ပြင်ဆင်တယ်။
      - **DELETE** – Table ထဲက Data ကို ဖျက်နိုင်ပါတယ်။

      ```sql
      INSERT INTO Customers (ID, Name, Age)
      VALUES (1, 'John Doe', 30);
      ```

   #### 3. Data Control Language (DCL)

   DCL Commands တွေက Database ထဲက Data တွေရဲ့ Access ကို Control လုပ်ပါတယ်။

   - **Common DCL Commands:**
      - **GRANT** – User တွေကို Database Access ပေးတယ်။
      - **REVOKE** – User တွေရဲ့ Database Access ကို ပိတ်တယ်။

      ```sql
      GRANT SELECT, INSERT ON Customers TO user_name;
      ```

   #### 4. Transaction Control Language (TCL)

   TCL Commands တွေက Database Transaction တွေနဲ့ ဆိုင်ပါတယ်။ Transaction က SQL Statements တွေကို Grouping လုပ်ထားတဲ့ Structure တစ်ခုဖြစ်ပါတယ်။

   - **Common TCL Commands:**
      - **COMMIT** – Transaction ကို Database မှာ permanently save လုပ်တယ်။
      - **ROLLBACK** – Transaction ကို ပြန်ဖျက်တယ်။
      - **SAVEPOINT** – Transaction ထဲမှာ Temporary Point တစ်ခု ထားတယ်။

      ```sql
      BEGIN TRANSACTION;
      INSERT INTO Customers (ID, Name, Age) VALUES (2, 'Jane Doe', 28);
      COMMIT;
      ```

#### SQL Constraints

   SQL Constraints တွေက Database ထဲမှာရှိတဲ့ Data တွေကို ကိုယ်ပိုင် Rules တွေသတ်မှတ်တာပါ။

   - **PRIMARY KEY** – Table ထဲမှာ Unique ဖြစ်ပြီး NULL မဖြစ်ရ။
   - **FOREIGN KEY** – တစ် Table ထဲက Data ကို တစ်ခြား Table နဲ့ Relationship တွဲပေးခြင်း။
   - **UNIQUE** – Column တစ်ခုက Value တွေကို Unique ဖြစ်ဖို့ ချထားတဲ့ Constraint ဖြစ်ပါတယ်။
   - **NOT NULL** – Value အနေနဲ့ NULL မရှိရပါဘူး။
   - **CHECK** – Value ကို Rule နဲ့ လိုက်ဖက်ဖို့ စစ်ကြည့်ပေးတယ်။

   ```sql
   CREATE TABLE Orders (
      OrderID INT PRIMARY KEY,
      ProductName VARCHAR(50) NOT NULL,
      Quantity INT CHECK (Quantity > 0)
   );
