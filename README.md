# likelionGit4
멋쟁이 사자처럼 스터디 깃 연습용 저장소
import requests
from bs4 import BeautifulSoup

url = "https://www.naver.com"

response = requests.get(url)
print(response.text[:500])

# print(type(response.text))

soup = BeautifulSoup(response.text, 'html.parser')
# print(BeautifulSoup(response.text, 'html.parser'))


file = open("naver.html", "w")
file.write(response.text)
file.close

print(soup.title)
print(soup.title.string)
print(soup.span)
print(soup.FindAll)
