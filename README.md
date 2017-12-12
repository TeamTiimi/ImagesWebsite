# netbeans
Team members Joni, Leo, Timi

Media sharing service done with servlets that can be used by anyone.
If the user wants to upload or comment he/she has to register and login to the website.
Login and logout are done with cookies.

Done with html, css, js, java, sql.

Software we used was Netbeans.

When designing the website we went mobile first.

Database:

create table User(
id int auto_increment not null,
name char(25),
email char(50),
username char(25),
password char(25),
primary key(id));
 
create table Comment(
id int auto_increment not null,
userid int,
comment char(100),
mediaid int,
primary key(id),
foreign key (userid) references User (id),
foreign key (mediaid) references Media (id)
);
 
create table Media(
id int auto_increment not null,
description char(25),
userid int,
url char(50),
primary key(id),
foreign key (userid) references User (id)
);

