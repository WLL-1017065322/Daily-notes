想apache一样的js

server.on('',function(){

var url=req.url

var filePath = '/index.html'

  if (url !== '/') {

​    filePath = url

  }

  fs.readFile(wwwDir + filePath, function (err, data) {

​    if (err) {

​      return res.end('404 Not Found.')

​    }

​    res.end(data)

  })

})



apache-完成目录列表渲染

1,如何得到wwwDir目录列表的文件名和目录名

fs.readder('d:/.../../',function(err,files){})

2

var fs=require('fs')

fs.readdir('C:/Users/Administrator/Desktop/www',function(err,file){

​    if(err){

​        return console.log(file)

​    }

​    console.log(file)

})

1. 如何得到 wwwDir 目录列表中的文件名和目录名

   fs.readdir

2. 如何将得到的文件名和目录名替换到 template.html 中

2.1 在 template.html 中需要替换的位置预留一个特殊的标记（就像以前使用模板引擎的标记一样）

 2.2 根据 files 生成需要的 HTML 内容

ps: // 在 EcmaScript 6 的 ` 字符串中，可以使用 ${} 来引用变量

server.on('request', function (req, res) {

  var url = req.url

  fs.readFile('./template.html',function(err,data){

​      if(err){

​          return res.end('404')

​      }

​      fs.readdir(wwwDir,function(err,file){

​          if(err){

​              return res.end('can not find www')

​          }

​         //console.log(file)

​          var content='';

​          file.forEach(function(item){

​              content+=`

​            <tr>

​              <td data-value="apple/"><a class="icon dir" href="C:/Users/Administrator/Desktop/www">${item}/</a></td>

​              <td class="detailsColumn" data-value="0"></td>

​              <td class="detailsColumn" data-value="1509589967">2017/11/2 上午10:32:47</td>

​            </tr>

​            `

​          })

​          data=data.toString()

​          //console.log(data)

​          data=data.replace('^_^',content)

​          console.log(data)

​          res.end(data)

​    })

  })

