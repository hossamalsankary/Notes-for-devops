# users

- ##### create eexpir date for user jane 
```diff
+ sudo usermod --expiredate  March 1, 2030   jane 
```
- ##### Create a system account called apachedev 
```diff

+ sudo useradd --system apachedev
```
- ##### Jane's account i.e jane is expired.Unexpire the same and make sure it never expires again. -e, --expiredate EXPIRE_DATE  set account expiration date to EXPIRE_DATE 
```diff

+ sudo usermod -e "" jane
```
- ##### Create a user account called jack and set its default login shell to be /bin/csh. 
```diff

+ sudo useradd --shell /bin/csh jack

```
- ##### Delete the user account called jack and ensure his home directory is removed. 
```diff

+ sudo userdel --remove jack
```
- ##### Mark the password for jane as expired to force her to immediately change it the next time she logs in. 
```diff

+ sudo chage -d '0' jane

```
- ##### Add the user jane to the group called developers. 
```diff

+ sudo usermod -a -G developers jane

```
- #####  Create a group named cricket and set its GID to 9875 .
```diff

+sudo groupadd --gid 9875 cricket

```
- ###### You already created group cricket in the previous question, now rename this group to soccer while preserving the same GID.
```diff

+ sudo groupmod -n soccer cricket

```
- ##### Create a user sam with UID 5322, also make it a member of soccer group. 
```diff

+ sudo useradd -G soccer sam  --uid 5322

```
- ##### Update primary group of user sam and set it to rugby 
```diff

+ sudo usermod -g rugby sam

```
- ##### Lock the user account called sam 
```diff

+ sudo usermod --lock sam

```
- ##### appdevsDelete the group called appdevs.
```diff

+ sudo groupdel appdevs

```
- ##### Make sure the user jane gets a warning at least 2 days before the password expires.  
```diff

+ sudo chage -W 2 jane

```