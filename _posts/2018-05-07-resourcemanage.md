---
layout: post
title: Asp.NET resource manage
categories: programming
tags: c#
author: Aemon
description: Via implement IDisposable interface to manage system resource by manually.
---

Via implement IDisposable interface to manage system resource by manually.

```c#
using System;

namespace Mod3_Lab1
{
    class Test : IDisposable
    {
        private bool isDisposed=false; //是否回收过 flag

        public int Age { get; set; }

        public Test(int age)
        {
            Age = age;
        }

        public void SetAge()
        {
            Console.WriteLine(Age);
        }

        ~Test() ////供GC调用的析构函数
        {
            Dispose(false);
        }
        //供程序员显式调用的Dispose方法
        public void Dispose()
        {
            Dispose(true);
            GC.SuppressFinalize(this);
        }

        //protected的Dispose方法, 保证不会被外部调用。
        protected void Dispose(bool disposing)
        {
            if (isDisposed)
            {
                return;
            }

            lock (this) //多线程情况下
            {
                if (disposing)
                {
                    //release managed object resource 加入此类调用了其它托管资源，比如其它的类
                    Console.WriteLine("Here is release managed object resource...");
                }
                //release unmanaged object resource  数据库连接，文件锁
                Console.WriteLine("Here is release unmanaged object resource...");
                isDisposed = true;
            }
        }
    }
}

```


```c#
using System;

namespace Mod3_Lab1
{
    class Program
    {
        static void Main(string[] args)
        {
            Test test=null;
            //call method 1
            try
            {
                test = new Test(18);
                test.SetAge();

            }
            catch (Exception ex)
            {
                Console.WriteLine(ex.Message);
            }
            finally
            {
                test.Dispose();
            }

            //call method 2
            using (test=new Test(20))
            {
                test.SetAge();
            }
        }
    }
}

```
