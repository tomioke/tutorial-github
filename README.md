Settings pertama git bash windows 10

buat folder .ssh di C:\Users\user
masuk git bash lalu ketikkan

$ cd ~/.ssh
$ ssh-keygen -t rsa -C "<your email>" -f "<name file>"
masukkan pharse atau password default enter saja tanpa password

cek dengan
ls -al ~/.ssh

Buka file .pub dengan notepad, copy semua script
Login ke akun github yang dituju, Masuk ke settings lalu Add Deploy Keys, pastekan skrip dan jangan lupa
Centang Allow Write Access

Kembali ke gitbash registrasikan
$ eval "$(ssh-agent -s)"
$ ssh-add ~/.ssh/<name file>

$ touch config           // Creates the file if not exists
$ code config            // Opens the file in VS code, use any editor

Untuk rubah ke account lain
$ ssh-add -D            //removes all ssh entries from the ssh-agent
$ ssh-add ~/.ssh/<nama file>                 // Adds the relevant ssh key

Contoh Push Program
echo "# tutorial-github" >> README.md
git init
git add README.md
Setting Repositori lokal
git config user.name "tomioke"   // Updates git config user name
git config user.email "tomiirvan@gmail.com"

git commit -m "first commit"
git branch -M master
git remote set-url origin git@github.com-tomioke:tomioke/tutorial-github.git
git remote add origin git@github.com:tomioke/tutorial-github.git
git push -u origin master
