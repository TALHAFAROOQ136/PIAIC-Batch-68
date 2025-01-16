# **`Dictionary`**
Python mein **dictionary** ek important data structure hai, jisme key-value pairs store kiye jaate hain. Aap ne jo methods mention kiye hain, wo sab dictionary ke saath use hote hain. In methods ka use aap different tasks ke liye kar sakte hain, jaise keys aur values ko access karna, nayi entries add karna, ya elements ko modify ya remove karna. Main aapko in sab methods ko explain kar raha hoon:

### 1. **`clear()`**
   - **Kaam**: Ye method dictionary ke sabhi elements ko remove kar deta hai, aur dictionary ko khali kar deta hai.
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   my_dict.clear()
   print(my_dict)  # Output: {}
   ```

### 2. **`copy()`**
   - **Kaam**: Ye method ek shallow copy banata hai dictionary ka, matlab original dictionary ko change kiye bina aap ek nayi copy bana sakte hain.
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   new_dict = my_dict.copy()
   print(new_dict)  # Output: {'apple': 1, 'banana': 2}
   ```

### 3. **`fromkeys()`**
   - **Kaam**: Ye method ek nayi dictionary banata hai jisme aap specific keys ko define karte hain, aur un keys ke liye ek initial value set karte hain.
   - **Use**:
   ```python
   keys = ["a", "b", "c"]
   new_dict = dict.fromkeys(keys, 0)
   print(new_dict)  # Output: {'a': 0, 'b': 0, 'c': 0}
   ```

### 4. **`get()`**
   - **Kaam**: Ye method dictionary mein specific key ki value ko retrieve karta hai. Agar key nahi hoti, to ye `None` return karta hai (ya aap default value de sakte hain).
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   print(my_dict.get("apple"))  # Output: 1
   print(my_dict.get("cherry", "Not Found"))  # Output: Not Found
   ```

### 5. **`items()`**
   - **Kaam**: Ye method dictionary ke sabhi key-value pairs ko return karta hai as a view object. Ye aapko tuples ki form mein keys aur values provide karta hai.
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   print(my_dict.items())  # Output: dict_items([('apple', 1), ('banana', 2)])
   ```

### 6. **`keys()`**
   - **Kaam**: Ye method dictionary ki saari keys ko return karta hai ek view object mein.
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   print(my_dict.keys())  # Output: dict_keys(['apple', 'banana'])
   ```

### 7. **`pop()`**
   - **Kaam**: Ye method ek specific key ko remove karta hai aur us key ki associated value return karta hai. Agar key nahi milti, to `KeyError` hota hai (agar default value specify na ki ho).
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   value = my_dict.pop("apple")
   print(value)  # Output: 1
   print(my_dict)  # Output: {'banana': 2}
   ```

### 8. **`popitem()`**
   - **Kaam**: Ye method dictionary ka last inserted key-value pair remove karta hai aur us pair ko return karta hai as a tuple. (Python 3.7+ mein order preserve hota hai).
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   last_item = my_dict.popitem()
   print(last_item)  # Output: ('banana', 2)
   print(my_dict)  # Output: {'apple': 1}
   ```

### 9. **`setdefault()`**
   - **Kaam**: Ye method check karta hai agar specified key dictionary mein hai. Agar key exist karti hai to uski value return karta hai, agar key nahi hoti to specified default value ko dictionary mein add karta hai aur wo value return karta hai.
   - **Use**:
   ```python
   my_dict = {"apple": 1}
   print(my_dict.setdefault("banana", 2))  # Output: 2
   print(my_dict)  # Output: {'apple': 1, 'banana': 2}
   ```

### 10. **`update()`**
   - **Kaam**: Ye method ek dictionary ko doosri dictionary ya key-value pairs ke saath update karta hai. Agar koi key pehle se exist karti hai to uski value ko overwrite kar deta hai.
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   my_dict.update({"banana": 3, "cherry": 4})
   print(my_dict)  # Output: {'apple': 1, 'banana': 3, 'cherry': 4}
   ```

### 11. **`values()`**
   - **Kaam**: Ye method dictionary ki saari values ko return karta hai ek view object mein.
   - **Use**:
   ```python
   my_dict = {"apple": 1, "banana": 2}
   print(my_dict.values())  # Output: dict_values([1, 2])
   ```

### Summary:
- **`clear()`**: Dictionary ko empty karne ke liye.
- **`copy()`**: Dictionary ka shallow copy banane ke liye.
- **`fromkeys()`**: Nayi dictionary banane ke liye with specified keys and optional value.
- **`get()`**: Key ki value ko retrieve karne ke liye (default value bhi set kar sakte hain).
- **`items()`**: Key-value pairs ko return karne ke liye.
- **`keys()`**: Saari keys ko return karne ke liye.
- **`pop()`**: Specific key ko remove karke value return karne ke liye.
- **`popitem()`**: Last inserted key-value pair ko remove karke return karne ke liye.
- **`setdefault()`**: Key ki value ko check karne ke liye aur agar key exist nahi karti to usko add karne ke liye.
- **`update()`**: Dictionary ko update karne ke liye with new key-value pairs.
- **`values()`**: Saari values ko return karne ke liye.

In methods ka use aap apne Python programs mein dictionary ke operations ko efficiently manage karne ke liye kar sakte hain.
