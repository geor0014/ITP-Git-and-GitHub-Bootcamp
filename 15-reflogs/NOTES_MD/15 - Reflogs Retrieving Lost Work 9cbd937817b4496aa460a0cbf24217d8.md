# 15 - Reflogs: Retrieving Lost Work

# Overview of this Section

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1.png)

## 15.1 Reflogs

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%201.png)

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%202.png)

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%203.png)

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%204.png)

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%205.png)

## 15.2 Limitations

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%206.png)

## 15.3 The Command

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%207.png)

### 15.3.1 The Output

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%208.png)

## 15.4 Reflog References

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%209.png)

### 15.4.1 Timed References

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2010.png)

## 15.5 Retrieving Lost Commits

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2011.png)

### 15.5.1 Example

- You made a mistake and you want to reset to a certain commit in the past

```bash
git log --oneline
```

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2012.png)

```bash
git reset --hard COMMIT_HASH
```

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2013.png)

<aside>
💡 This will take is to the commit: `add more greens` and will **DELETE** our work **AFTER** that commit

</aside>

- Ten you realize that you did not want to actually `reset --hard` and you need to retrieve your work, but the commits are not gone

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2014.png)

<aside>
💡 Thankfully that information is still available in the **REFLOGS**

</aside>

```bash
git reflogs show master
```

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2015.png)

<aside>
💡 The commit hash we deleted can **STILL** be seen and is **AVAILABLE** and we can `checkout` and access it.

</aside>

<aside>
💡 To **UNDO** the deletion of that commit

</aside>

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2016.png)

<aside>
💡 You can either use `master{1}` or the specific **commit hash** `fb5072a`

</aside>

- If we now do a `git log --oneline` we can see that the commit is back

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2017.png)

## 15.6 Undoing a Rebase with Reflogs

- We create a **new file(`flowers.txt`)** and **branch(`flowers`)** to store plants in and we add flowers and commits

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2018.png)

We are now going to **REBASE** until the `add some zinnians`  commit

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2019.png)

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2020.png)

- Now our `git log --oneline`looks like this:

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2021.png)

We Decide that we want to **REBASE** further and make more changes

```bash
git rebase -i HEAD~2
```

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2022.png)

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2023.png)

- We decide that we made a **MISTAKE** and we want those individual commits back

```bash
git reflogs show **flowers**
```

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2024.png)

We want to go back to the `add celosia` commit, when we had all the commits and the old name

```bash
git reset --hard **c47ecfc OR flowers{2}**
```

```bash
git log --oneline
```

![1.png](15%20-%20Reflogs%20Retrieving%20Lost%20Work%209cbd937817b4496aa460a0cbf24217d8/1%2025.png)