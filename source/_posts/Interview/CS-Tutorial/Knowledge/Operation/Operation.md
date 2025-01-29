
## Operation


### Other Software

#### 1.VS Code
- `cmd+ O`: open multiple windows
- `command+shift+P`: open Terminal -(Select the "Preview" option)


#### 2.Mac

##### 2.1 VIM
- `fn(earth)+E`: emoji 

#### Terminal Overview

##### 1. General
- Open Terminal: `command +space`
- find the dict location：`cd`
- print the path of current dict:`pwd`
- print all the fiels in the current dict:`ls`
- creat new file: `touch`
- create new dict: `mkdir`
- remove files/dict:`rm`
- move file/dict:`mv`
- copy file:`cp`
- space problem: `add quote`

##### 2.Files
- write something into txt file: `echo`
- show the content in txt file: `cat`
- delete all the content in txt file `truncate -s 0`
- replace/print content `sed`
- print specific content `awk`

##### 3.Regex
- ` grep -E`
- `grep-Ei`

```text
echo "specific_word" | grep -E '^specific_word$'   # 匹配整个字符串必须完全等于 "specific_word"
echo "SPECIFIC_WORD" | grep -Ei '^specific_word$'  # 匹配整个字符串 "specific_word"（忽略大小写）
echo "A" | grep -E '.'                             # 匹配任何非空字符
echo "The number is 7" | grep -E '[0-9]'           # 匹配至少包含一个数字的行
echo "Order 12345 is confirmed" | grep -E '[0-9]+' # 匹配一个或多个连续的数字
echo "abc123" | grep -E '[[:alnum:]]'              # 匹配至少包含一个字母或数字
echo "Hello World" | grep -E '[[:space:]]'         # 匹配至少包含一个空格的行
echo "start_of_string is here" | grep -E '^start_of_string' # 匹配以 "start_of_string" 开头的行
echo "This ends with end_of_string" | grep -E 'end_of_string$' # 匹配以 "end_of_string" 结尾的行
echo "I choose option1" | grep -E '(option1|option2)' # 匹配 "option1" 或 "option2"

echo {1..5}   # Expands to: 1 2 3 4 5
echo {a..e}   # Expands to: a b c d e
```

##### 4.loop
```text
# 使用 for 循环写入 Line1-Line10 到 text.txt
for i in {1..10}; do echo "Line $i" >> text.txt; done  # 逐行追加 "Line X" 到 text.txt

# use for to write the fruits into text.txt
for item in apple banana cherry; do
    echo "Fruit: $item"
done

#iterate the files in the dict
for file in *.txt; do
    echo "Processing $file"
done


# while 循环逐行读取文件内容
while read line; do
    echo "Line: $line"
done < text.txt  # 逐行读取 text.txt 并输出

# set the ending point of while
count=1
while [ $count -le 5 ]; do
    echo "Count: $count"
    ((count++))
done

# use until to set the ending point
count=1
until [ $count -gt 5 ]; do
    echo "Count: $count"
    ((count++))
done

# use list to print
list=("apple" "banana" "cherry")
echo "${list[@]}" # all
echo "${list[0]}" # the first
list=$(seq 1 5) # from the 1st to the 5th
echo "$list"
```

##### 5. Application

```python
mkdir /Users/evelyndu/new_dict
cp test.csv /Users/evelyndu/ #no change on the file name
cp test.csv /Users/evelyndu/test_backup #change on the file name
cp -R /Users/evelyndu/Downloads /Users/evelyndu/Downloads_backup

echo "Line" >>test.txt
truncate -s 0 test.txt
sed 's/apple/banana' test.txt #first apple for each line
sed 's/apple/banana/g' test.txt # all apples for each line
sed -n '5p' test.txt #print 5th line
sed '3d' test.txt delete 3rd line
sed '3i\foo\'  test.txt  
#insert the new 3rd row
awk '{print $2, $4}' students.txt
awk '$3 > 50 {print $1, $3}' numbers.txt

```

##### 6.Example

To extract valid phone numbers from file.txt that match the required formats (xxx) xxx-xxxx or xxx-xxx-xxxx, we can use the grep command with a regular expression.
```python
grep -E "^(\([0-9]{3})\ [0-9]{3}-[0-9]{4}|[0-9]{3}-[0-9]{3}-[0-9]{4}))$"
```