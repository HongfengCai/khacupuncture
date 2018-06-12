---
layout: post
title: C# Object Oriented Accompanying Theories
categories: programming
tags: c#
author: Aemon
description: some theries here about c# OOP
---

<dl>
	<dt>What is a user interface?</dt>
		<dd>- The part of the application that the user interacts with. Such as From1.</dd>
	<dt>In a command line enviroment, what determines the order in which things happen?</dt>
		<dd>- The program and the value of the variables.</dd>
	<dt>In an event driven environment, what determines the order in which things happen?</dt>
		<dd>- The user.</dd>
		<dd>- The user triggers events that drive the program.</dd>
	<dt>What is the difference between a project and a namespace?</dt>
		<dd>- The project is the collection of C# files that belong to a single application. Some files are automatically created. Others are created by the programmer.</dd>
		<dd>- The namespace is a container for the classes.</dd>
	<dt>Describe the difference between design-time and run-time.</dt>
		<dd>- Design time describes the stage where the GUI is built and the associated code is written.</dd>
		<dd>- Runtime is when the application is running.</dd>
	<dt>What is class?</dt>
		<dd>- class is a sort of datatype.</dd>
		<dd>- class is a description or sepecification of the available states, and accompanying behaviours.</dd>
		<dd>- class is an encapsulation of the data that is stored in the fields and the methods that operate on that data.</dd>
	<dt>What is an object?</dt>
		<dd>- object is an instance of a class.</dd>
		<dd>- The implementation/instantiation of a class</dd>
	<dt>What is an instance of a class?</dt>
		<dd>- An object.</dd>
	<dt>What is a UML class diagram used for?</dt>
		<dd>- A UML Class Diagram is a display/diagramming tool for showing the three parts of a class: the name, fields and methods contained in a class.</dd>
		<table style="width:250px; margin-left:40px;">
		  <thead>
			<tr>
			  <th>Class Name</th>
			</tr>
		  </thead>
		  <tbody>
			<tr>
			  <td>Fields <br/>with their data types</td>
			</tr>
			<tr>
			  <td>Methods <br/>including the constructor</td>
			</tr>
		  </tbody>
	</table>
	<dt>What is a constructor?</dt>
		<dd>- constructor is a method that is executed to create an object.</dd>
		<dd>- constructor is a method with no return type and the same name as the class.</dd>
		<dd>- constructor is a method that is used to initialize the fields with data.</dd>
	<dt>A class is sometimes described as a blueprint, explain what this means.</dt>
		<dd>- Think of a blueprint or plan for a house. The blueprint is not the actual house, but is the detailed description for a house.</dd>
		<dd>- You use the blueprint to build a house.</dd>
		<dd>- The blueprint provides sufficient detail so that house can be built.</dd>
		<dd>- From one blueprint you can build any number of houses.</dd>
	<dt>List the key components of a class</dt>
		<dd>- class header: public class ClassName</dd>
		<dd>- constants</dd>
		<dd>- fields</dd>
		<dd>- constructor</dd>
		<dd>- methods</dd>
		<dd>- properties</dd>
	<dt>What is another name for a field?</dt>
		<dd>- private data member</dd>
	<dt>What happens when a constructor is called?</dt>
		<dd>- The fields are populated with data.</dd>
		<dd>- The fields are given initial values.</dd>
		<dd>- The act of populating the fields creates an object.</dd>
	<dt>When you pass an object that is an instance of a class as an argument, what is passed into the parameter variable?</dt>
		<dd>- A reference to the object.</dd>
		<dd>- Describe two examples of passing an object that is an instance of a class that you used this week.(random or pictureBox1)</dd>
	<dt>What is abstraction?</dt>
		<dd>- The essential characteristics of an object that distinguish it from other objects and thus provides crisply defined conceptual boundaries</dd>
		<dd>- An entity, in terms of its functionality and interface, not its implementation.</dd>
	<dt>What is encapsulation?</dt>
		<dd>- Information hiding</dd>
		<dd>- A class hides its internal details so that the rest of the program does not need to know or understand how they work, but just how to use them.</dd>
	<dt>Why is the keyword "this" used?</dt>
		<dd>- Used as prefix to the field name</dd>
		<dd>- Distinguishes the fedld name from the parameter name</dd>
	<dt>Why is the class given public scope?</dt>
		<dd>- Because the object is created and used outside its class</dd>
	<dt>Why are the fields private?</dt>
		<dd>- To protect the data that is stored in the fields.</dd>
		<dd>- To provide encapsulation of the object</dd>
	<dt>A method can have private or public visibility. How is this shown in the code?</dt>
		<dd>- Public or private keyword in method signature</dd>
		<dd>- Private method names begin with lower cae letter(camelCase); Public methods begin with uppercae letter(PascalCase)</dd>
		<dd>- In class diagram, "+" signifies public and "-" signifies private.</dd>
	<dt>Why are properties used in OO programming?</dt>
		<dd>- To set/get field values from outside the class</dd>
		<dd>- To check legal/legitimate values are used to set a field value.</dd>
		<dd>- To provide control of legal access when getting field values.</dd>
	<dt></dt>
		<dd></dd>
		<dd></dd>
		<dd></dd>
</dl>
