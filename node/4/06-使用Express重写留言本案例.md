post.html:

form  action="/post" method="post"><form>

app.js:

app.get('/pinglun',function(req,res){

​     console.log(req.query)

​    // res.render('post.html',{

​    //     title:'管理系统'

   // })

​    var comment=req.query

​    comment.dataTime='2017-11-5 10:58:51'

​    comments.unshift(comment)

​    //res.status=302

​    //res.setHeader('Location','/')

​    res.redirect('/')

})