#### Paginator
Paginator is a pagination plugins, It is easy to use, and nice looking appearance.

![]()

##### Example

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <link rel="stylesheet" href="../src/paginator/css/paginator.css">
</head>
<body>

<div id="paginator" class="paginator">

</div>


<script src="../src/paginator/js/jquery.min.js"></script>
<script src="../src/paginator/js/paginator.js"></script>
<script>
    $(function () {
        var s = $('#cur').val();
        console.log(s);
        paginator.generPageHtml({
            //当前页
            pno :1,
            //总页码
            total :100,
            //总数据条数
            totalRecords : 1000,
            //链接前部
            hrefFormer : '',
            //链接尾部
            hrefLatter : '',
            //链接算法
            getLink : function(n){
                if(n == 1){
                    return this.hrefFormer + this.hrefLatter;
                }
                return this.hrefFormer  + '#' + this.hrefLatter;
            }

        });
    })
</script>

</body>
</html>

```