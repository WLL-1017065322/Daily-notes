index.html

<td>{{ $index+1 }}</td>

​                  <a href="/students/edit?id={{ $value._id }}">编辑</a>

​                  <a href="/students/delete?id={{ $value._id }}">删除</a>

edit.html

<input type="hidden" name="id" value="{{ student._id }}">