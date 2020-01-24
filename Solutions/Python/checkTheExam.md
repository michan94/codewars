## Problem

The first input array contains the correct answers to an exam, like ["a", "a", "b", "d"]. The second one is "answers" array and contains student's answers.

The two arrays are not empty and are the same length. Return the score for this array of answers, giving +4 for each correct answer, -1 for each incorrect answer, and +0 for each blank answer(empty string).

If the score < 0, return 0.

### Examples

* checkExam(["a", "a", "b", "b"], ["a", "c", "b", "d"]) → 6

* checkExam(["a", "a", "c", "b"], ["a", "a", "b",  ""]) → 7

* checkExam(["a", "a", "b", "c"], ["a", "a", "b", "c"]) → 16

* checkExam(["b", "c", "b", "a"], ["",  "a", "a", "c"]) → 0


**First Solution:**
```python
def check_exam(arr1,arr2):
  score = 0;
  if len(arr1) != 0 and len(arr2) != 0:
    if len(arr1) == len(arr2):
      while len(arr1) > 0 and len(arr2) > 0:
          correct = arr1.pop(0);
          answer = arr2.pop(0);
          if answer == "":
            score += 0;
          if answer != "" and answer != correct:
            score -= 1;
          if correct == answer:
            score += 4;
  if score < 0:
    return 0;
  return score;
```    
