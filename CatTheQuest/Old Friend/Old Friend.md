# Old Friend

This challenge was really fun, I would say I enjoyed this challenge most this year.

## Description

We are given this information

```Our dear H4z4rd is back, do you remember him? He remembers you. He has used the same communication place as last time for your next mission. Complete it.```

## Solution

You need to take a look on his social media profile an there are new posts
![X-Profile](https://github.com/KarpatenWilli/CTF_Writeups/blob/796c3ab973f399101dc4189ab3d113bebfe1d582/CatTheQuest/Old%20Friend/Images/X1.png)

First of all you find a this strange code and need do decrypt it

```_y @ i_ _he __y _o __c_y_t```

This part took too long for me, but after many tries, I found out what it should mean.

```My @ is the key to decrypt```


Now you have to find a tool to decrypt these emojis. After some googling, I came across the following page: https://txtmoji.com/Decrypt the Emojis with his X-Username to get the key.

![](https://github.com/KarpatenWilli/CTF_Writeups/blob/b23df46146e9d77f2a787449396d60b858c6c959/CatTheQuest/Old%20Friend/Images/txtmoji.png)

Key: ```https://riddle.catthequest.com/```

![](https://github.com/KarpatenWilli/CTF_Writeups/blob/9513d8fd3fe2a66a4c9dab5a30fcdcf086c9ad59/CatTheQuest/Old%20Friend/Images/Riddle.png)

Now you take a deeper look in the source code and found this text file https://cdn.cattheflag.org/riddle.txt

There you get these long B64 code that you have to decode several times
```Vm0wd2QyUXlVWGxWV0d4V1YwZDRWMVl3WkRSWFJteFZVMjA1VjAxV2JETlhhMk0xVmpKS1IySkVUbGhoTWsweFZqQmFZV015U2tWVWJHaG9UVlZ3VlZadGNFdFRNVWw1VTJ0V1ZXSkhhRzlVVmxaM1ZsWmFkR05GWkZwV01VcEpWbTEwYTFkSFNrZGpTRUpYVFVad1NGUlVSbUZrUlRGWlkwZDRVMkpXU2twV2JURXdWakZXZEZOclpGaGlSMmhoV1ZSS2IxSkdXbGRYYlhSWFRWaENSbFpYZUZOVWJVWTJVbFJDVjAxdVVuWldha3BIVWpGT2RWUnRjRk5pVjJoWFZtMTBWMlF5VWxkalJtaHNVakJhY1ZscmFFTlNiRnBZWlVoa1YwMUVSbGRaTUZaelZqSktWVkZZYUZkaGEzQklXWHBHVDJSV1ZuUmhSazVzWWxob1dGWnRNSGRsUjBsNFUydGtXR0V5VWxsWmJHaFRWMFpTVjJGRlRsUmlSM1F6VjJ0U1UxWnJNWEpYVkVwWFlsaFNNMVpxU2t0V1ZrcFpXa1pvVjJKV1NrbFhXSEJIVkRKU1YxWnVUbGhpVjNoVVdWUk9RMWRHV25STlZFSlhUVlV4TkZaWGRHdFdNV1JJWVVac1dtSkdXbWhaTVZwaFpFZE9ObEpzYUdsU00yaFlWbXBLTkZReFdsaFRhMlJxVWtWYVYxWnFUbTlsYkZweFVtMUdVMkpWVmpaWlZWcHJZVWRGZUdORVdsZGlXRUpJVmtSR2ExWXlUa1phUjJoVFRXNW9WVmRXVWs5Uk1XUnpWMWhvWVZKRlNtRldiWE40VGtaa2NsWnRkRmROYTNCNVZHeGFjMWR0U2tkWGJXaFhZVEZ3VkZacVJtdGtWbkJHVGxaT2FXRXdjRWxXYlhCTFpXczFWMWRzYUZSaE1sSnhWVzE0ZDFkR2JITmhSazVPVFZad2VGVnRNVWRWTWtwV1lrUmFXR0V4Y0ROWmEyUkdaV3hHY21KR2FGaFRSVXBKVm10U1MxUnRWbGRVYmtwaFVteEtjRlpxVG05V1ZtUlhWV3M1VWsxWFVsaFdNV2h2VjJzd2VWVnJPVmRpV0ZKWVZHeGFZV1JGTlZaUFYyaHBVbGhDV2xac1pEUmpNV1IwVTJ0a1dHSlhhRmhaVkVaM1lVWndSbHBHVGxSU2EzQXdXbFZrYzFVeVNuSlRhM1JYVFc1b1dGZFdXbEpsVmtweVdrWlNXRkl5YUZwWFZ6QjRUa1paZUZWc1pHRlNlbXhQVkZaYWQyVkdWblJrU0dScFVqQndWMVl5ZEhkV01ERjFZVWRvV2xaWFVrZGFWV1JQVTBVNVYxcEhiRmhTVlhCS1ZqRmFVMU14VVhsVVdHaHFVbGQ0Vmxsc1pHOVdSbEpZVFZjNWJHSkhVbGxhVldNMVlWVXhXRlZ1Y0ZkTlYyaDJWakJrUzFKck5WZFdiRlpYWWtoQ1dWWkhkR0ZaVjFKSVZXdG9hMUp0VW5CV2JHaERUbXhhVlZOVVJsVk5WbkF3VlRKNGMxWnRSbkpPVjBaVlZucFdkbFpyV21GalZrcDBaRWQwVTJFelFYZFhiRlpoWVRKR1YxcEZaRk5oYkhCWVdWZDBkbVF4V2xWU2JGcHNVbTFTTVZVeWN6RldNa3BYVTI1b1YxWXphSEpaYWtaclVqRldjMkZGT1ZkV1ZGWldWbGN4TkdReVZrZFdibEpPVmxkU1dGUlZVa2RsVmxKelZtMDVWMDFWYnpKVmJYUnZWakZhUmxkcmVGZGhhM0JRVlcxNFlXTXhjRWhpUms1T1ZsWlplbFp0ZUdGVk1VbDRZa1prV0dKcmNFOVdiWGgzVjBac1dXTkdaRmRTYkZwNVZtMTBZVlF4VmxWTlJHczk=```

Enter the "answer" on https://riddle.catthequest.com/ to get the flag.

## Flag

```CAT{77ce9338-MjAyNC0wNy0xOSAxNDo0MjoxOA--82da432fa256993bc1ba619856dfc3bf71ef56f64d9e8e28745986e37314edf5}```
