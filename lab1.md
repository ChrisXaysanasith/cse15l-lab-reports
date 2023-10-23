# Lab Report 1

## cd, ls, and cat usage

**cd**

* cd with no arg
  
![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/047793fc-f5b6-4f3d-854f-947ca292c2f1)

The usage of change directory with no arg brings you back to the /home directory, or so called home directory of the user. For example if I cd into lecture1 it will be `/home/lecture1`, but if I cd it makes the working path `/home`

* cd with a path arg

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/2163b7ec-7144-453e-8b44-a5218532201b)

Changing the directory with an argument results in going into the relative path `./lecture1` , making the working path `/home/lecture1`

* cd with a path to file arg

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/858cbc5e-ae65-479c-ba77-f20ef0c9cb87)

Changing the directory with an argument to a file results to an error, because we are trying to access a working path `/home/lecture1/Hello.java` which is a folder that holds the file therefore it will error because it is accessing a file, not the folder. 

---

**ls**

* ls with no arg

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/eb058c44-08ae-476e-b324-dcf74eb3eca6)

The usage of list, gives the files and folders in the given directory which the directory we will be working with is `/home` and the contents in `/home`. working path is `/home`

* ls with a path arg

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/0391bbeb-6cf7-43ea-abd9-71a6ef3b769a)

I am listing the directory of the working path `/home/lecture1/messages` therefore the files that are listed contain the contents of `Hello World!` in a certain language file

* ls with a path to file arg

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/1aa7eaa0-733b-488e-a833-42a142467fb8)

The way I am listing the path to a file only lists the working path `/home/lecture1/messages/en-us.txt` for the file

---

**cat**

* cat with no arg

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/568f7382-c1cf-4c1d-a38c-792fe2a04976)

The concatenate outputs nothing from the working path theres no argument to print out the content of a file
* cat with a path arg, working path is `/home/`

![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/5531532b-06b0-4893-8915-da9b15430874)

The concatenate outputs from the working path `/home/lecture1/messages` which states that it is a directory for the usage of cat, therefore an error occurs as its not reading a file rather it outputs that its a directory

* cat with a part to file arg
  
![Image](https://github.com/ChrisXaysanasith/cse15l-lab-reports/assets/26499648/0edec8b9-43db-48fe-8086-8b6213c16484)

The concatenate outputs the file `Hello World` from the working path `/home/lecture1/messages/en-us.txt`


