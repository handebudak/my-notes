# Logical Operators (Mantıksal Operatörler)

1. **Ve Operatörü (&&)**:
- **`&&`** operatörü, iki koşulun da doğru olması durumunda ifadeyi doğru olarak değerlendirir.
- Her iki koşul da doğruysa, ifade doğru olur.
- Eğer en az bir koşul yanlışsa, ifade yanlış olur.
- Örneğin: **`if (x > 5 && y < 10) { ... }`**
2. **Veya Operatörü (||)**:
- **`||`** operatörü, iki koşuldan en az birinin doğru olması durumunda ifadeyi doğru olarak değerlendirir.
- Her iki koşul yanlışsa, ifade yanlış olur.
- Eğer en az bir koşul doğruysa, ifade doğru olur.
- Örneğin: **`if (x === 0 || y === 0) { ... }`**
3. **Değil Operatörü (!)**:
- **`!`** operatörü, bir koşulun tersini alır.
- Eğer koşul doğruysa, **`!`** operatörü onu yanlış olarak değerlendirir.
- Eğer koşul yanlışsa, **`!`** operatörü onu doğru olarak değerlendirir.
- Örneğin: **`if (!isLoggedin) { ... }`**