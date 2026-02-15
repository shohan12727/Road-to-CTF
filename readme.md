## 🛡️ Cybersecurity Platforms

- 🔐 **TryHackMe** – https://tryhackme.com  
  Hands-on labs for learning cybersecurity, Linux, networking, and penetration testing.

- 🧠 **Hack The Box** – https://www.hackthebox.com  
  Advanced penetration testing labs simulating real-world security challenges.


from crypto.Util.number import inverse, long_to_bytes

n = 13870167871170603539853823667358484046902421629948955717529720761283300290610951171995255725756077115552991490101550908835761582533097315003928621785718862
e = 65537
c = 4295326297043518525183203754014861225101389475437884646394740539903871496726408992789066821276030688663458898323001928086374963190129850231307669598082735


p = 2
q = n // p

z = (p-1) * (q-1)

d = inverse(e, z)

m = pow(c,d,n)


ans = (long_to_bytes(m))
print(ans.decode())