<!doctypehtml>
<html>

<head>
    <title>Taehoonysos Calculator</title>
    <meta charset="utf-8">
    <script>
        function insert(num) {
            document.form.textview.value = document.form.textview.value + num;
        }

        function equal() {
            var exp = document.form.textview.value;
            if (exp) {
                document.form.textview.value = eval(exp);
            }
        }

        function clean() {
            document.form.textview.value = "";
        }

        function back() {
            var exp = document.form.textview.value;
            document.form.textview.value = exp.substring(0, exp.length - 1);
        }
    </script>
    <style>
        body {
            color: rgb(9, 9, 77);
            background-color: rgb(219, 185, 185)
        }
        
        .button {
            width: 100px;
            height: 90px;
            font-size: 50px;
            margin: 2px;
            cursor: pointer;
            background: rgb(105, 61, 61);
            border: none;
            color: rgb(219, 185, 185);
        }
        
        .textview {
            width: 405px;
            margin: 5px;
            font-size: 50px;
            padding: 8px;
            border: solid;
            color: black;
        }
        
        .main {
            position: absolute;
            top: 30%;
            left: 35%;
            transform: translateY(-20%);
        }
        
        .bg {
            background: linear-gradient(to right, rgb(161, 101, 101), rgb(118, 118, 221));
            height: 77%;
        }
    </style>
</head>

<body>
    <h1 style="font-family:fantasy;">
        <center>Taehoon's Calculator</center>
    </h1>
    <div class="main bg">
        <form name="form">
            <input class="textview" name="textview">
        </form>
        <table>
            <tr>
                <td><input class="button" type="button" value="C" onclick="clean()"></td>
                <td><input class="button" type="button" value="/" onclick="insert('/')"></td>
                <td><input class="button" type="button" value="x" onclick="insert('*')"></td>
                <td><input class="button" type="button" value="<--" onclick="back()"></td>
            </tr>
            <tr>
                <td><input class="button" type="button" value="7" onclick="insert(7)"></td>
                <td><input class="button" type="button" value="8" onclick="insert(8)"></td>
                <td><input class="button" type="button" value="9" onclick="insert(9)"></td>
                <td><input class="button" type="button" value="-" onclick="insert('-')"></td>
            </tr>
            <tr>
                <td><input class="button" type="button" value="4" onclick="insert(4)"></td>
                <td><input class="button" type="button" value="5" onclick="insert(5)"></td>
                <td><input class="button" type="button" value="6" onclick="insert(6)"></td>
                <td><input class="button" type="button" value="+" onclick="insert('+')"></td>
            </tr>
            <tr>
                <td><input class="button" type="button" value="1" onclick="insert(1)"></td>
                <td><input class="button" type="button" value="2" onclick="insert(2)"></td>
                <td><input class="button" type="button" value="3" onclick="insert(3)"></td>
                <td rowspan=3><input class="button" style="height: 188px" type="button" value="=" onclick="equal()"></td>
            </tr>
            <tr>
                <td colspan=2><input class="button" style="width: 210px;" type="button" value="0" onclick="insert(0)"></td>
                <td><input class="button" type="button" value="." onclick="insert('.')"></td>
            </tr>
        </table>
    </div>

</body>

</html>
