### 基本數據類型

C++ 提供了多種基本數據類型，用於存儲整數、浮點數、字符等。這些包括：

- `int`：存儲整數。
- `float` 和 `double`：用於存儲帶有小數的數字。
- `char`：存儲單個字符。
- `bool`：存儲布爾值（`true` 或 `false`）。

### 輸入/輸出

C++ 使用 `cin` 進行輸入和 `cout` 進行輸出，這些都定義在 `iostream` 頭文件中。

### 條件判斷：if-else 語句

用於基於條件執行不同的代碼塊。

### 範例代碼

```cpp
#include <iostream>
using namespace std;

int main() {
    // 定義基本變量
    int myInt;
    float myFloat;
    char myChar;
    bool myBool;

    // 從用戶輸入獲取數據
    cout << "Enter an integer: ";
    cin >> myInt;

    cout << "Enter a float number: ";
    cin >> myFloat;

    cout << "Enter a character: ";
    cin >> myChar;

    cout << "Enter a boolean value (0 or 1): ";
    cin >> myBool;

    // 使用 if-else 條件語句
    if (myBool) {
        cout << "Boolean value is true." << endl;
    } else {
        cout << "Boolean value is false." << endl;
    }

    // 顯示輸入的值
    cout << "Integer: " << myInt << endl;
    cout << "Float: " << myFloat << endl;
    cout << "Character: " << myChar << endl;

    return 0;
}
```


### 3. 迴圈

在 C++ 中，迴圈用於重複執行一段代碼。主要有三種類型的迴圈：

- **for 迴圈**：當你知道需要執行迴圈的確切次數時使用。
- **while 迴圈**：當你想要迴圈持續執行直到某個條件不再滿足時使用。
- **do-while 迴圈**：類似於 while 迴圈，但它至少執行一次代碼塊。

### 4. 陣列

陣列是一種存儲固定大小的相同類型元素的集合。在 C++ 中，陣列的大小必須在編譯時已知。

### 範例代碼

```cpp
#include <iostream>
using namespace std;

int main() {
    // 定義一個整數陣列
    int numbers[5];
    
    // 使用 for 迴圈來填充陣列
    cout << "Enter 5 integers:" << endl;
    for (int i = 0; i < 5; i++) {
        cin >> numbers[i];
    }

    // 使用 while 迴圈來顯示陣列內容
    int j = 0;
    cout << "You entered:" << endl;
    while (j < 5) {
        cout << numbers[j] << " ";
        j++;
    }
    cout << endl;

    // 使用 do-while 迴圈進行簡單的選單
    int choice;
    do {
        cout << "\nEnter 0 to exit, 1 to display array: ";
        cin >> choice;

        if (choice == 1) {
            for (int i = 0; i < 5; i++) {
                cout << numbers[i] << " ";
            }
            cout << endl;
        }
    } while (choice != 0);

    return 0;
}
```

### 5. 函數

函數是一段可以重複使用的代碼塊，它可以執行特定的任務。函數可以有參數，並且可以返回值。

### 6. 引用和指針

- **引用**：一種特殊的數據類型，它是另一個變量的別名。
- **指針**：一種存儲變量內存地址的變量。

### 7. 結構體

結構體是一種允許我們將不同類型的數據存儲在同一單位的複合數據類型。

### 範例代碼


```cpp
#include <iostream>
using namespace std;

// 定義一個結構體
struct Person {
    string name;
    int age;
};

// 函數原型
void printPersonInfo(const Person &p);
void updateAge(Person *p, int newAge);

int main() {
    Person person = {"Alice", 30};

    // 顯示初始信息
    printPersonInfo(person);

    // 更新年齡
    updateAge(&person, 35);
    cout << "After updating age:" << endl;
    printPersonInfo(person);

    return 0;
}

// 函數定義
void printPersonInfo(const Person &p) {
    cout << "Name: " << p.name << ", Age: " << p.age << endl;
}

void updateAge(Person *p, int newAge) {
    p->age = newAge; // 使用指針更新年齡
}
```
