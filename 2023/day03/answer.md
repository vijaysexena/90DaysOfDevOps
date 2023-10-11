# Basic Linux Commands

1. To view what's written in a file.
   ` cat filename`

2. To change the access permissions of files.
   ``chmod 777 folder_name/ file_name`

3. To check which commands you have run till now.
   `history`

4. To remove a directory/ Folder.
   `rm folder_name`

5. To create a fruits.txt file and to view the content.
   create file --> ` cat >> fruits.txt` then add content
   view file --> `cat fruits.txt ` or `vi fruits.txt`

6. Add content in devops.txt (One in each line) - Apple, Mango, Banana, Cherry, Kiwi, Orange, Guava.

   1. `nano devops.txt` or `vi devops.txt`

      1. `echo "apple" >> devops.txt`
      2. `echo "Mango" >> devops.txt`
      3. `echo "Banana" >> devops.txt`
      4. `echo "Cherry" >> devops.txt`
      5. `echo "Kiwi" >> devops.txt`
      6. `echo "Orange" >> devops.txt`
      7. `echo "Guava" >> devops.txt`

7. To Show only top three fruits from the file.
   `head -n 3 file_name`

8. To Show only bottom three fruits from the file.
   `tail -n 3 file_name`

9. To create another file Colors.txt and to view the content.
   create file -> `touch Colors.txt`
   view file -> `cat Colors.txt`

10. Add content in Colors.txt (One in each line) - Red, Pink, White, Black, Blue, Orange, Purple, Grey.

    1. `nano Colors.txt` or `vi Colors.txt`

       1. `echo "Red" >> Colors.txt`
       2. `echo "Pink" >> Colors.txt`
       3. `echo "White" >> Colors.txt`
       4. `echo "Black" >> Colors.txt`
       5. `echo "Blue" >> Colors.txt`
       6. `echo "Orange" >> Colors.txt`
       7. `echo "Purple" >> Colors.txt`
       8. `echo "Grey" >> Colors.txt`

11. To find the difference between fruits.txt and Colors.txt file.

    `diff fruits.txt Colors.txt`
