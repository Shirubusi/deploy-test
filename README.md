# create-react-appで作成したアプリをGitHubで公開するまで
**予めGitHubでリポジトリを作成しておく(ユーザー名とリポジトリ名が必要になるため)

**1.create-react-app　*アプリ名はリポジトリ名と同じにした方が望ましい

npx create-react-app "アプリ名"


**2.ディレクトリ移動

cd "アプリ名"

**3.gh-pagesをインストール

npm install gh-pages --save-dev


**4.pakage.jsonに"homepage","predeploy","deploy"を追記

---pakage.json---
"homepage":"https://"ユーザー名".github.io/"リポジトリ名"",

  "scripts": {
    ...,
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    ...
  },


**5.init

git init

**6.remote

git remote add origin https://github.com/"ユーザー名"/"リポジトリ名".git


**7.add

git add .


**8.commit

git commit -m "コメント"


**9.deploy

npm run deploy


**10.push

git push -u origin master


ここまでの流れでアプリをGitHubで公開できます。
