# python-learn
#学生信息管理系统（python）
import os.path

filename='student.txt'
def main():
    while True:
        menum()
        choice=int(input('请选择'))
        if choice in [0,1,2,3,4,5,6,7]:
            if choice ==0:
                answer=input('您确定要退出系统吗？y/n')
                if answer=='y'or answer=='Y':
                    print('谢谢您的使用！！！')
                    break #退出系统
                else:
                    continue
            elif choice==1:
                insert()#录入学生信息
            elif choice==2:
                search()
            elif choice==3:
                delete()
            elif choice==4:
                modify()
            elif choice==5:
                sort()
            elif choice==6:
                total()
            elif choice==7:
                show()
        else:
            continue

def menum():
    print('===============学生信息管理系统================')
    print('----------------功能菜单---------------------')
    print('\t\t\t\t\t\t1、录入学生信息')
    print('\t\t\t\t\t\t2、查找学生信息')
    print('\t\t\t\t\t\t3、删除学生信息')
    print('\t\t\t\t\t\t4、修改学生信息')
    print('\t\t\t\t\t\t5、排序')
    print('\t\t\t\t\t\t6、统计学生总人数')
    print('\t\t\t\t\t\t7、显示所有学生信息')
    print('\t\t\t\t\t\t0、退出')
    print('-----------------------------------------')

def insert():
    student_list=[]
    while True:
        id=input('请输入id（如1001）')
        if not id:
            break
        name=input('请输入姓名')
        if not name:
            break

        try:#加一个小循环
            englist=int(input('请输入英语成绩：'))
            python=int(input('请输入python成绩：'))
            java=int(input('请输入Java成绩：'))
        except:
            print('输入无效，不是整数类型，请重新输入。')
            continue
        #将录入的学术信息保存到字典当中
        student={'id':id,'name':name,'english':englist,'python':python,'java':java}
        #将学生信息添加到列表中
        student_list.append(student)
        answer=input('是否继续添加？y/n\n')
        if answer=='y':
            continue
        else:
            break

    #调用save（）函数
    save(student_list)
    print('学生系统录入完毕！！！！')

def save(lst):
    try:
        stu_txt=open(filename,'a',encoding='utf-8')#创建或追加

    except:
        stu_txt=open(filename,'w',encoding='utf-8')#创建或覆盖
    for item in lst:
        stu_txt.write(str(item)+'\n')
    stu_txt.close()


def search():
    while True:
        flag=False
        student_query=[]
        num=int(input('输入姓名查询请按1，输入ID查询请按2'+'\n'))
        if num in[1,2]:
            if num==1:
                student_name=input('请输入要查询的学生姓名:')
                if os.path.exists(filename):
                    with open(filename, 'r', encoding='utf-8') as file:
                        student_old = file.readlines()  # 输出结果为列表 ['{1001}']
                else:
                    student_old = []
                if student_old:
                    with open(filename, 'r', encoding='utf-8') as rfile:
                        d = {}
                        for item in student_old:
                            d = dict(eval(item))  # 将字符串转成字典
                            if d['name'] == student_name:
                                student_query.append(d)
                                show_student(student_query)
                                flag=True
                                break
                            else:
                                continue
                        if flag:
                            print(f'已经查询到名字为{student_name}相关的学生信息')
                        else:
                            print(f'抱歉，没有查询到名字为{student_name}相关的学生信息')
                else:
                    print('无学生信息')
            elif num==2:
                student_id = input('请输入要查询的学生ID:')
                if os.path.exists(filename):
                    with open(filename, 'r', encoding='utf-8') as file:
                        student_old = file.readlines()  # 输出结果为列表 ['{1001}']
                else:
                    student_old = []
                if student_old:
                    with open(filename, 'r', encoding='utf-8') as rfile:
                        d = {}
                        for item in student_old:
                            d = dict(eval(item))  # 将字符串转成字典
                            if d['id'] == student_id:
                                student_query.append(d)
                                show_student(student_query)
                                flag = True
                                break
                            else:
                                continue
                        if flag:
                            print(f'已经找到ID为{student_id}的学生信息')
                        else:
                            print(f'抱歉，没有查询到ID为{student_id}的学生信息')
                else:
                    print('无学生信息')
            answer=input('是否继续查询学生信息y/n:')
            if answer=='y':
                continue
            else:
                break

        else:
            print('输入错误，请重新输入')
            continue

def show_student(lst):
    format_title='{:^6}\t{:^12}\t{:^8}\t{:^10}\t{:^10}\t{:^8}'
    print(format_title.format('ID','姓名','英语成绩','python成绩','java成绩','总成绩'))
    format_data='{:^6}\t{:^12}\t{:^8}\t{:^10}\t{:^10}\t{:^8}'
    for item in lst:
        print(format_data.format(item['id'],
                                  item['name'],
                                  item['english'],
                                  item['python'],
                                  item['java'],
                                  int(item['english'])+int(item['python'])+int(item['java'])
                                 )
              )

def delete():
    while True:
        student_id=input('请输入要删除的学生ID')
        if student_id!='':
            if os.path.exists(filename):
                with open(filename,'r',encoding='utf-8')as file:
                    student_old=file.readlines()#输出结果为列表 ['{1001}']
            else:
                student_old=[]
            flag=False #标记是否删除
            if student_old:
                with open(filename,'w',encoding='utf-8') as wfile:
                    d={}
                    for item in student_old:
                        d=dict(eval(item))#将字符串转成字典
                        if d['id']!=student_id:
                            wfile.write(str(d)+'\n')
                        else:
                            flag=True
                    if flag:
                        print(f'id为{student_id}的学生信息已被删除')
                    else:
                        print(f'没有找到ID为{student_id}的学生信息')
            else:
                print('无学生信息')
                break
                show()#删除之后要重新显示所有学生信息
                answer=input('是否继续删除?y/n\n')
                if answer=='y':
                    continue
                else:
                    break
def modify():
    show()
    if os.path.exists(filename):
        with open(filename,'r',encoding='utf-8')as rfile:
            student_old=rfile.readlines()
    else:
        return
    student_id=input('请输入要修改的学员的ID：')
    with open(filename,'w',encoding='utf-8') as wfile:
        for item in student_old:
            d=dict(eval(item))
            if d['id']==student_id:
                print('找到学生信息，可以修改他的相关信息了！')
                show()
                while True:
                    try:
                        d['name']=input('请输入姓名:')
                        d['english']=input('请输入英语成绩:')
                        d['python']=input('请输入python成绩:')
                        d['java']=input('请输入Java成绩:')
                    except:
                        print('您的输入有误，请重新输入！！！')
                    else:
                        break
                wfile.write(str(d)+'\n')
                print('修改成功！！！')
            else:
                wfile.write(str(d)+'\n')
        answer=input('是否继续修改其他学生的信息：y/n')
    if answer=='y':
        modify()



def sort():
    show()
    if os.path.exists(filename):
        with open(filename,'r',encoding='utf-8') as rfile:
            student_list=rfile.readlines()
        student_new=[]
        for item in student_list:
            d=eval(item)
            student_new.append(d)
    else:
        return
    asc_or_desc=int(input('请选择（0.升序 1.降序）：'))
    if asc_or_desc==0:
        asc_or_desc=False
    elif asc_or_desc==1:
        asc_or_desc=True
    else:
        print('你的输入有误，请重新输入')
        sort()
    mode=input('请选择排序方式（1.按英语成绩排序 2、按python成绩排序 3、按Java成绩排序 0、按总成绩排序：')
    if mode=='1':
        student_new.sort(key=lambda x:int(x['english']),reverse=asc_or_desc)
    elif mode=='2':
        student_new.sort(key=lambda x: int(x['python']), reverse=asc_or_desc)
    elif mode=='3':
        student_new.sort(key=lambda x: int(x['java']), reverse=asc_or_desc)
    elif mode=='0':
        student_new.sort(key=lambda x: int(x['english'])+int(x['java'])+int(x['python']), reverse=asc_or_desc)
    else:
        print('你的输入有误，请重新输入！！！')
        sort()
    show_student(student_new)
def total():
    if os.path.exists(filename):
        with open(filename,'r',encoding='utf-8')as rfile:
            students=rfile.readlines()
            if students:
                print(f'一共有{len(students)}名学生')
            else:
                print('还没有录入学生信息')
    else:
        print('暂未保存数据')

def show():
    student_lst=[]
    if os.path.exists(filename):
        with open(filename,'r',encoding='utf-8')as rfile:
            students=rfile.readlines()
            for item in students:
                student_lst.append(eval(item))
            if student_lst:
                show_student(student_lst)
    else:
        print('暂未保存数据！！！')


if __name__ == '__main__':
    main()
