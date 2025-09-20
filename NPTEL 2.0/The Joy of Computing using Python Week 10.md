# The Joy of Computing using Python

# Week 10

# Programming Assignment 1

```bash
def mentors(scores_dataset, subject):
    mentorships = {}

    for mentorG in scores_dataset:
        mentor_seq = mentorG['SeqNo']
        mentor_score = mentorG.get(subject)
        mentees = []

        for mentee in scores_dataset:
            mentee_seq = mentee['SeqNo']
            mentee_score = mentee.get(subject)

            if mentor_seq != mentee_seq:
                diff = mentor_score - mentee_score
                if 10 <= diff <= 20:
                    mentees.append(mentee_seq)

        mentorships[mentor_seq] = mentees

    return mentorships
```

# Programming Assignment 2

```bash
def get_summary(trans):
    summ = []

    for txn in trans:
        tid = txn['TID']
        cost = sum(item['Price'] * item['Qty'] for item in txn['Items'])
        summ.append({'TID': tid, 'Cost': cost})

    return summ
```

# Programming Assignment 3

```bash
def compress(notice):
    if not notice:
        return ""

    result = []
    count = 1

    for it in range(1, len(notice)):
        if notice[it] == notice[it - 1]:
            count += 1
        else:
            result.append(notice[it - 1] + (str(count) if count > 1 else ''))
            count = 1

    # Handle the last character group
    result.append(notice[-1] + (str(count) if count > 1 else ''))

    return ''.join(result)
```

### Congratulations 🎉 You Completed Assignment !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

# [MY SWAYAM](https://www.youtube.com/@MySwayam)
