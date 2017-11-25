<!--page_number: true-->



![bg original](back.jpg)

<h2 style="text-align:center"><font color="white">Well-Defined Code Structure</font></h2>

---

## 1. Python

```python
def main(): # 메인함수가 결과를 계산 및 Print
    result = Calc(10000)
    print(result)
    
def Calc(n): # 계산 코드는 main 밑에다가!
    s = 0
    for i in range(0, n):
        s += i
    return s
    
if __name__ == "__main__": # 메인함수를 돌려라!
    main()
```

---

## 1. Python

* 컴파일 언어들은 모두 main 함수를 내장하고 있어서, 결과를 출력 및 기록하는 것은 모두 main 함수에서 실행
* C 같은 구식 언어를 제외하면 Top - Down 식 접근법이 가능하여 main부터 짜고 구체적인 계산은 밑에 구성
* Python은 밑에 있는 함수를 원칙적으로 위에서 받아올 수 없지만, magic script를 이용하면 Interpreter가 한 번 순회한 후 실행이 가능하여 흉내를 낼 수 있음.

---

## 2. R

```R

CalcSampleCov <- function(x, y, verbose = TRUE) {
  # Computes the sample covariance between two vectors.
  #
  # Returns:
  #   The sample covariance between x and y.
  n <- length(x)
  # Error handling
  if (n <= 1 || n != length(y)) {
    stop("Arguments x and y have different lengths: ",
         length(x), " and ", length(y), ".")
  }
  if (TRUE %in% is.na(x) || TRUE %in% is.na(y)) {
    stop("x and y must not have missing values.")
  }
  cov <- var(x, y)
  if (verbose)
    cat("Covariance = ", round(cov, 4), ".\n", sep = "")
  return(cov)
}
```

---

## 2. R

* R은 Python이나 기타 언어에 있는 main 기능을 대체할 수단이 마땅치 않음. 따라서 Top - Down Approach는 사용하기 힘듬.
* R Studio에서 처럼 function으로 Wrap 하지 않고 코딩하는 것은 지양해야 함. 앞의 예시처럼 꼭 function으로 wrap한 다음 return한 값을 이용하는 것이 좋음. (캡슐화)
* Google이 배포한 [R Style Guide](http://dialektike.github.io/Rguide.xml)를 참조
(**HW #1** R Style Guide로 책에서 공부한 코드 짜기)

---
