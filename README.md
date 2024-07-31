Introduction

A secure one-way hash function needs to satisfy two properties: the one-way property and the collision resistance property. The one-way property ensures that given a hash value h , it is computationally infeasible
to find an input M , such that hash(M) = h . The collision-resistance property ensures that it is computationally infeasible to find two different inputs M1 and M2 , such that hash(M1) = hash(M2) .
Several widely-used one-way hash functions have trouble maintaining the collision-resistance property. At
the rump session of CRYPTO 2004, Xiaoyun Wang and co-authors demonstrated a collision attack against
MD5 2
. In February 2017 , CWI Amsterdam and Google Research announced the SHAttered attack ,
which breaks the collision-resistance property of SHA-1 3
.
While many students do not have trouble understanding the importance of the one-way property, they cannot easily grasp why the collision-resistance property is necessary, and what impact these attacks can cause.
The learning objective of this lab is for students to really understand the impact of collision attacks, and
see in first hand what damages can be caused if a widely-used one-way hash function’s collision-resistance
property is broken. To achieve this goal, students need to launch actual collision attacks against the MD5
hash function. Using the attacks, students should be able to create two different programs that share the
same MD5 hash but have completely different behaviors. This lab covers a number of topics described in
the following:
• One-way hash function, MD5
• The collision-resistance property
• Collision attacks

Lab Environment.
The lab uses a tool called “Fast MD5 Collision Generation”, which was written by Marc Stevens; the
name of the binary is called md5collgen in our VMs. md5collgen has already been installed inside
/home/seed/bin
