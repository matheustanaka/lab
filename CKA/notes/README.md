# Tips and tricks

When you apply for CKA, pay attention here. You can follow the tips below to save your time during the exam.

# 1. Less command - to read files

You can use the command less to read files. The less command enable you to use vim key-bindings, so it's more easy to navigate and filter for a content

```shell
k run -h | less
```

Then, when you get into the "less" mode you can navigate with "hjkl" keys and also use "/" to filter for a specifc content.


### Reminder

Imagine you are on less mode and you have to filter for "dry-run" word, you can use "/" and then type dry-run to filter each reference inside the docs.

Then, you have to use "n" to find the next occurence and "N" to go back to the previous version.

# 2. Copying things from Kubernetes Documentation on website

Let's suppose you want to copy an yaml from documentation. If you paste the content on "vim" the yaml file will be pasted without the correct identation.


So, to avoid this behaviour you can use the flag below to save your time and ident your yaml.


**Press : and then type set paste to insert the paste mode.**


This mode will help you ident the file when you paste yaml content

# 3. Copying YAML files directly from the terminal

You want to be fast, just run the command below to copy an yaml file directly on the terminal

```shell
# Prints the content of the nginx image without create the pod
# --dry-run enables you to see the content of the image without create the pod

k run nginx-yaml --image=nginx --dry-run=client -o yaml

# Convert the content directly into a new file
k run nginx-yaml --image=nginx --dry-run=client -o yaml > nginx.yaml
```
