# Twitter trends
"""Twitter shows trends in order to make its users aware of the trending news. These trends are nothing but trending hashtags that the users are tweeting about. For example: If thousands of users are talking about United States by adding a hashtag #US in their tweet, then US will be a trending hashtag. Couple of example tweets with hashtag #US could be:

Donald Trump becomes the 45th #US President Roger Federer wins #US Open for 5th time Given a list of N tweets, your task is to find top the five trending hashtags. Each tweet, let's call it S, will contain at least one one word with hashtag. There will be maximum of three hashtags in any tweet. All hashtags in a single tweet will be unique.

Note: Any tweet is composed of lowercase and uppercase English letters, digits and spaces. Any hashtag begins with # and the subsequent characters will only contain lowercase and uppercase English letters and digits.

Input Format

First line of the input will contain N denoting the number of tweets. Next N lines, each will contain a string S.

Constraints

none

Output Format

Print the top five trending hashtags. In case of tie between any two hashtags, print them in lexicographical order in a new line."""




e=int(input())
n=""
for i in range(e):
    n+=input()+" "
l=n.split(" ")
a=[]
d={}
for s in l:
    if s=="":
        pass
    elif s[0]=="#":
        a.append(s)
for i in a:
    f=l.count(i)
    d[i]=f
s= dict(sorted(d.items(), key=lambda x: x[0]))
so= dict(sorted(s.items(),key=lambda x: x[1],reverse=True))
h=0
for i in so.keys():
    h=h+1
    print(i)
    if h==5:
        break
