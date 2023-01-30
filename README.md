# Day 1
#### Q-1.1
```sql
create table EMP (
    EMPNO   number(6),
    ENAME   varchar(20),
    JOB     varchar(10),
    MGR     number(4),
    DEPTNO  number(3),
    SAL     number(7,2)
);
```
#### Output: Table created.

#### Q-1.2
```sql
desc EMP;
```

#### Output:
|TABLE |EMPResult |Set 1
|:-:|:-:|:-:|
|Column	Null?	|Type
|EMPNO	|- 	    |NUMBER(6,0)
|ENAME	|- 	    |VARCHAR2(20)
|JOB	    |- 	    |VARCHAR2(10)
|MGR	    |- 	    |NUMBER(4,0)
|DEPTNO	|- 	    |NUMBER(3,0)
|SAL	    |- 	    |NUMBER(7,2)

#### Q-1.3
```sql
insert into EMP values (7369, 'SMITH', 'CLERK', 7566, 20, 800);
insert into EMP values (7399, 'ASANT', 'SALESMAN', 7566, 20, 1600);
insert into EMP values (null, 'WARD', 'SALESMAN', null, null, 800);
insert into EMP values (7369, 'JONES', 'MAAGER', 5975, 20, 5975);
```

#### Output: 1 row(s) inserted. (x4)

#### Q-1.4
```sql
select EMPNO from EMP where EMPNO is null;
```

#### Output:
EMPNO

`-`

#### Q-1.5
```sql
drop table EMP;

create table EMP (
    EMPNO   number(6),
    ENAME   varchar(20),
    JOB     varchar(10),
    MGR     number(4),
    DEPTNO  number(3),
    SAL     number(7,2)
);

insert into EMP values (7369, 'SMITH', 'CLERK', 7566, 20, 800);
insert into EMP values (7399, 'ASANT', 'SALESMAN', 7566, 20, 1600);
insert into EMP values (7499, 'ALLEN', 'SALESMAN', 7698, 30, 1600);
insert into EMP values (7521, 'WARD', 'SALESMAN', 7698, 30, 1250);
insert into EMP values (7566, 'JONES', 'MANAGER', 7839, 20, 5975);
insert into EMP values (7698, 'BLAKE', 'MANAGER', 7839, 30, 9850);
```

#### Output: 1 row(s) inserted. (x5)

#### Q-1.6
```sql
select * from EMP;
```
#### Output:
|EMPNO	|ENAME	|JOB			|MGR		|DEPTNO	|SAL
|:--:|:-:|:-:|:-:|:-:|:-:|
|7399		|ASANT	|SALESMAN	|7566		|20		|1600
|7566		|JONES	|MANAGER		|7839		|20		|5975
|7499		|ALLEN	|SALESMAN	|7698		|30		|1600
|7521		|WARD	|SALESMAN	|7698		|30		|1250
|7698		|BLAKE	|MANAGER		|7839		|30		|9850
|7369		|SMITH	|CLERK		|7566		|20		|800

#### Q-1.7
```sql
select EMPNO, ENAME, SAL from EMP;
```
#### Output:
|EMPNO|ENAME	|SAL
|:---:|:---:|:--|
|7399|ASANT|1600
|7566|JONES|5975
|7499|ALLEN|1600
|7521|WARD|1250
|7698|BLAKE|9850
|7369|SMITH|800

#### Q-1.8
```sql
select * from EMP where SAL > 1500;
```

#### Output:
|EMPNO|ENAME	|JOB	|MGR	|DEPTNO|SAL
|:-:|:-:|:-:|:-:|:-:|:-:|
|7399|ASANT	SALESMAN		|7566		|20		|1600
|7566|JONES	MANAGER		|7839		|20		|5975
|7499|ALLEN	SALESMAN		|7698		|30		|1600
|7698|BLAKE	MANAGER		|7839		|30		|9850


#### Q-1.9
```sql
select EMPNO, SAL from EMP where JOB = 'SALESMAN';
```

#### Output:
|EMPNO	|SAL
|:-:|:-:|
|7399|1600
|7499|1600
|7521|1250
