
#画蝴蝶#
```
import turtle as t
def draw_recursive_wings(size):
    """绘制4个小翅膀"""
    for i in range(4):
            t.seth(90 * (i + 1))
            t.circle(size,90)
            #-90,0,90,180
            t.seth(-90 + i * 90)
            t.circle(size,90)
    size += 50
    if size <= 200:
        draw_recursive_wings(size)
def main():
    #主函数 顺便试试turtle其他命令
    t.penup()
    t.pendown()
    t.pensize(3)
    t.color("pink")
    size = 50
    draw_recursive_wings(size)
    t.exitonclick()
if __name__ == "__main__" :
	main()
```



```
#画小树#
import turtle

def draw_branch(branch_length):
    if branch_length>=5:
        #绘制右侧树枝
        turtle.forward(branch_length)
        turtle.right(20)
        draw_branch(branch_length-5)
        #绘制左侧树枝
        turtle.left(40)
        draw_branch(branch_length-5)
        #返回根节点
        turtle.right(20)
        turtle.backward(branch_length)
def main():
    turtle.penup()
    turtle.backward(40)
    turtle.pendown()
    turtle.left(90)
    turtle.pencolor("pink")
    draw_branch(50)
    turtle.done()
if __name__ == "__main__" :
    main()
```
