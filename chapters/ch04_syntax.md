## 第4章 基本文法

### 4.1 変数とデータ型

#### 4.1.1 変数の宣言と初期化

**Python:**
```python
x = 5
y = 3.14
name = "Alice"
```

**C++:**
```cpp
int x = 5;
double y = 3.14;
std::string name = "Alice";
```

Pythonでは、変数を宣言する際にデータ型を明示する必要はありません。しかし、C++では変数を宣言する際にデータ型を明示する必要があります。また、C++ではセミコロン `;` を使用して文の終わりを示します。

#### 4.1.2 基本データ型

**Python:**
- 整数型：`int`
- 浮動小数点型：`float`
- 文字列型：`str`
- 論理型：`bool`

**C++:**
- 整数型：`int`, `short`, `long`, `long long`
- 浮動小数点型：`float`, `double`, `long double`
- 文字型：`char`
- 論理型：`bool`
- 文字列型：`std::string`（標準ライブラリ）

C++では、整数型や浮動小数点型に複数のサイズが存在し、用途に応じて適切な型を選択する必要があります。

### 4.2 基本的な入出力

#### 4.2.1 コンソールへの出力

**Python:**
```python
print("Hello, World!")
```

**C++:**
```cpp
#include <iostream>

int main() {
    std::cout << "Hello, World!" << std::endl;
    return 0;
}
```

Pythonでは、`print` 関数を使用してコンソールに出力しますが、C++では `std::cout` を使用します。また、`#include <iostream>` を使って入出力ストリームをインクルードする必要があります。

#### 4.2.2 コンソールからの入力

**Python:**
```python
name = input("Enter your name: ")
```

**C++:**
```cpp
#include <iostream>
#include <string>

int main() {
    std::string name;
    std::cout << "Enter your name: ";
    std::cin >> name;
    return 0;
}
```

Pythonでは `input` 関数を使用してユーザーからの入力を受け取りますが、C++では `std::cin` を使用します。また、文字列を扱うために `#include <string>` を追加する必要があります。

### 4.3 演算子と制御構造

#### 4.3.1 演算子

**Python:**
```python
a = 10
b = 5
print(a + b)  # 足し算
print(a - b)  # 引き算
print(a * b)  # 掛け算
print(a / b)  # 割り算
print(a % b)  # 剰余
print(a ** b) # 累乗
```

**C++:**
```cpp
#include <iostream>

int main() {
    int a = 10;
    int b = 5;
    std::cout << a + b << std::endl;  // 足し算
    std::cout << a - b << std::endl;  // 引き算
    std::cout << a * b << std::endl;  // 掛け算
    std::cout << a / b << std::endl;  // 割り算
    std::cout << a % b << std::endl;  // 剰余
    std::cout << pow(a, b) << std::endl; // 累乗
    return 0;
}
```

基本的な演算子はPythonとC++でほぼ同じですが、累乗演算子はPythonでは `**` を使用しますが、C++では `pow` 関数を使用します。

#### 4.3.2 条件分岐

**Python:**
```python
x = 10
if x > 0:
    print("x is positive")
elif x == 0:
    print("x is zero")
else:
    print("x is negative")
```

**C++:**
```cpp
#include <iostream>

int main() {
    int x = 10;
    if (x > 0) {
        std::cout << "x is positive" << std::endl;
    } else if (x == 0) {
        std::cout << "x is zero" << std::endl;
    } else {
        std::cout << "x is negative" << std::endl;
    }
    return 0;
}
```

条件分岐の構文はPythonとC++で似ていますが、C++では `else if` を使い、各ブロックを `{}` で囲む必要があります。

#### 4.3.3 繰り返し

**Python:**
```python
for i in range(5):
    print(i)

i = 0
while i < 5:
    print(i)
    i += 1
```

**C++:**
```cpp
#include <iostream>

int main() {
    for (int i = 0; i < 5; i++) {
        std::cout << i << std::endl;
    }

    int i = 0;
    while (i < 5) {
        std::cout << i << std::endl;
        i++;
    }
    return 0;
}
```

Pythonの `for` ループでは `range` 関数を使用しますが、C++では初期化、条件、更新を `for` 文内で指定します。`while` ループの構文は両言語で似ていますが、C++では `{}` を使用します。
