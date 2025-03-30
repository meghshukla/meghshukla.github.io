---
name: "Towards Self-Supervised Covariance Estimation in Deep Heteroscedastic Regression"
slug: toss
tools: [Method]
image: https://raw.githubusercontent.com/deep-regression/deep-regression.github.io/master/files/images/toss/toss.png
description: '<img src="https://iclr.cc/static/core/img/ICLR-logo.svg" alt="ICLR Logo" style="width: 100px; height: auto;">'
---

<script>
    MathJax = {
        tex: {
        inlineMath: [['$', '$'], ['\\(', '\\)']]
        }
    };
    </script>
<script type="text/javascript" id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

<style>
.responsive-video {
  width: 100%;
  height: auto;
  max-width: 100%;
}
</style>


# Towards Self-Supervised Covariance Estimation in Deep Heteroscedastic Regression
<br><br>
<span style="font-size:20px;">**Megh Shukla**, Aziz Shameem, Mathieu Salzmann, Alexandre Alahi  <br>
*International Conference on Learning Representations (ICLR) 2025, Singapore*</span>

<a href="https://openreview.net/forum?id=Q1kPHLUbhi"><img alt="OpenReview" src="https://img.shields.io/badge/ICLR%202025-OpenReview%20(link)-black?style=flat&logo=data%3Aimage%2Fjpeg%3Bbase64%2C%2F9j%2F4AAQSkZJRgABAQAAAQABAAD%2F4gKgSUNDX1BST0ZJTEUAAQEAAAKQbGNtcwQwAABtbnRyUkdCIFhZWiAH5AADABkACQAOAABhY3NwQVBQTAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA9tYAAQAAAADTLWxjbXMAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAtkZXNjAAABCAAAADhjcHJ0AAABQAAAAE53dHB0AAABkAAAABRjaGFkAAABpAAAACxyWFlaAAAB0AAAABRiWFlaAAAB5AAAABRnWFlaAAAB%2BAAAABRyVFJDAAACDAAAACBnVFJDAAACLAAAACBiVFJDAAACTAAAACBjaHJtAAACbAAAACRtbHVjAAAAAAAAAAEAAAAMZW5VUwAAABwAAAAcAHMAUgBHAEIAIABiAHUAaQBsAHQALQBpAG4AAG1sdWMAAAAAAAAAAQAAAAxlblVTAAAAMgAAABwATgBvACAAYwBvAHAAeQByAGkAZwBoAHQALAAgAHUAcwBlACAAZgByAGUAZQBsAHkAAAAAWFlaIAAAAAAAAPbWAAEAAAAA0y1zZjMyAAAAAAABDEoAAAXj%2F%2F%2FzKgAAB5sAAP2H%2F%2F%2F7ov%2F%2F%2FaMAAAPYAADAlFhZWiAAAAAAAABvlAAAOO4AAAOQWFlaIAAAAAAAACSdAAAPgwAAtr5YWVogAAAAAAAAYqUAALeQAAAY3nBhcmEAAAAAAAMAAAACZmYAAPKnAAANWQAAE9AAAApbcGFyYQAAAAAAAwAAAAJmZgAA8qcAAA1ZAAAT0AAACltwYXJhAAAAAAADAAAAAmZmAADypwAADVkAABPQAAAKW2Nocm0AAAAAAAMAAAAAo9cAAFR7AABMzQAAmZoAACZmAAAPXP%2FbAEMABQMEBAQDBQQEBAUFBQYHDAgHBwcHDwsLCQwRDxISEQ8RERMWHBcTFBoVEREYIRgaHR0fHx8TFyIkIh4kHB4fHv%2FbAEMBBQUFBwYHDggIDh4UERQeHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHh4eHv%2FAABEIAMgAyAMBIgACEQEDEQH%2FxAAdAAEAAgIDAQEAAAAAAAAAAAAABgcFCAEDBAIJ%2F8QAUhAAAQMDAQQEBwsGCwcFAAAAAQIDBAAFEQYHEiExE0FRYQgUInGBkbEVFjI0QlJzkpOhwSMkMzVy0SU2Q0RFU1RVY3SyFyZWYoLC4TdkdYPw%2F8QAGwEAAgMBAQEAAAAAAAAAAAAAAAMCBAUBBgf%2FxAAxEQABBAICAQMCBAQHAAAAAAABAAIDEQQFEiExExRBBlEiMmFxI5GhsRUkJVKBwdH%2F2gAMAwEAAhEDEQA%2FANy6UoOuhCUpShCUr4ccQgZWtKR3nFcghScpIIPI1HkLpC%2BqVSm1Tbg%2Fpe5SbVbNLTnXmFFCpUxCm2CR1px8Id%2BRVK6g227QrwVAXoQGlckQkBsD%2Fq4n76c2MuUC8BbpuOIbTvOLShI61HArxrvFqQrdVcoSSOoyED8a0DnX693BanJt3nyVHmXJCjn76xyvKUVL8o9p4mmCD7lR9Rfoci72tat1FyhqPYH0H8a9bbiHE7yFJUnqKTkV%2BcyDuK3keSe0cKylr1Hf7Y4HLderhFUORbkKH41z0PsUeov0HpWnGl9vOvbQUply2LuwDxRLR5RH7Y4%2BvNXRoLb5pK%2Frbi3YOWOarA%2FLHeZUe5Y5emoOjc1SDwVb9K62Hmn2UvMuIcbWMpWhWQR3GuylqaUpShCUpShCUpShCUpShCUpShCV4rxMMG3uykoCygcia9teO7RPH4LsXf3N%2FwCVjOKrZfq%2Bi70vzV1%2B66PPaw9l1E7cLgiMqMlAUCchWeVSMVH7Rp0W6amWZRXug8N3Fe83y1AkGY3kVk6vIyMfH%2F1F4DyerI8KTgCelxf7YbnESyl3o8K3s4zXrgMeLQ2mCoKLaAnOOdfUWQ1JZDzDgcbPIioZerzcWbrJZaklKErwkYHCo7HOxNafeOBJdQ6Q1pd0pnIYYkNlqQy082eBS4gKB9BqKztmOgZ0lcmVpS1rdV8JQZ3c%2BqsfFvt0VJaQqUogrSCMDjxqfDlVnUbqLZtc6IEcfuuOZx8qiNtWxJifa4bugrNbociOpZkNJO4p5JHAAnhkca1tv1lu1hnKg3q3SYEgfIeQU58x5H0V%2BhJxWN1BYLLf4Zh3q2RZ7Gc7j7YVjzHmK3GT0Eoxgr8%2BPVT1VvJ%2Fsp2c%2FwDCFq%2Bz%2FwDNc%2F7KNnH%2FAAfavs6Z7lpUPSK0apVteFFp2x6b1jb4lhtke3sLglxaGU4Clbx4mslO2PWOPsW9%2B6bhcDN8QRJ6ElPR7xIGOWccaZzFAqPHulD9mG1TUuhpCGo76ptrKvykJ9WU4%2F5D8k%2FdW22zrXdh1xZ%2FH7PIy4gAPxl8HWVdhH48q0NrLaS1Hd9LXxm8WWUqPJaPH5rietKh1g1x8Qd4XWPryv0ESciuahOyPaDbde6eEyNusT2MJmRSri2rtHak9RqbDlVQgg0U4dpSlKF1KUpQhKUpQhKUpQhKUpkUIXw5%2BjV5qq1X6RfnNWmcKBHA15fc6BxzEY%2BoK8v9Q6N%2B1DCx4HG0yN3FeLR36hZ859tRHUP67l%2Ft1YLLTbLfRtIShI5AcBXyqNGWoqUw0pR5kpFc2OiObgx4vMAtrtDX8TaraH8cZ%2BkT7asK%2BLW3Z5K21FKktkgjmK7xEig5EdoEcjuCuZcduVGWw7ncWMKwccKNRoH63GljD7LvH8kOeHFV3Duk8zWEmY8QXEgje5jNS3XDjjOn3FtuKQrfTxScHnXLWlrU26l1KHd5CgoflDzBrjXLTz%2Bn3W2GluL30%2BSkZPOq2Hrc3CwJ2zu5OI67JXHEHwq7XPm8fzuR9of31N9mz7r9rkqedccIfwCtROPJHbUFXbLnx%2FMJJ%2F8ArNTnZpHkR7VJTJZcZUX8gLTjI3RWX9NMyRmgycqo%2BbSQTaoDwxkL9%2FVqWUK3DAICscCd85FU6q83dUHxBV2uBibu70BkrLeOzdzjHdW9evdH2XWdictV5jhaCMtPJGHGVdSknqNazXDwdtdtTn2oZt0qMlZDTyn9wrT1EjHA19OjkbVFRc03YVP0qda72U6t0ZZBdr21DTFLqWstPhZ3jnHD0VBaeCD4S%2B1INn2q7no3U8e9WxZ3mzuvNE%2BS82TxQfw7DW%2BVqlifbI05KFNpkModCVc07wzg%2BuvztreHYjqy3ao0FbVxpCDLix0MSmd7y21pGMkdhxnPfSJx8pkZ%2BFOqUyKVXTUpSlCEpSlCEpSlCFxzrFamkJZtLyN8pccG62AeJPdUdc1RckurSEs4CiB5NZPTQVdHl3OarpHGzuNpx5KO8Dtryo30GyccTGvkbFn4HyUzgW9ldWjGp6Jb5lJeSncGC5nGc12a5edZYjFp1beVHO6rHVUlAqL6%2B%2BLxv2z7KhssQ6%2FSyRMeSR8%2FPlDTblGPHJf9qf8ArmslpmVJXe46FyHVJJOQVkg8KwxIFZHSis6gj%2Bc%2ByvnepyJ3ZkVvP5h8lOcAB4U9uDyo8F59IBLaCoZ7qhJ1rcAPi8f76mN84WaX9Er2VUSlcK9z9UbHKxJWCB9WP%2B1VsAKUq1xcR%2FNo331kNMaqmXS8ohPMMoQpCiSnOeFV%2BtXOs7s6VnVTX0a%2FZWVq9vnS5UbHyEgkWl8%2B6VpqISMkgCvjpmf6xH1hWL1oSnS1xUCQegPKqTW%2B5j9IvH7Rr1%2B03AwJGs4XY%2B6jLN6a2A6dn%2BtR9YV9oUFDKSCO0GtdVvO%2F1i%2FrGrm2ZKKtGwyVFRO9xJz1mu6zc%2B%2BkLOFdfdLhyBK6qUC8Lv8A9LWv%2FkWvYqtfthNpt172o2q2XaI3LhvdJ0jLg8lWEkitp9uukZOs9nsu2QV7sxlYkx09TikZ8n0gmtO9JX656P1QzeILTaZ8NS0hD6MhKsFKgR3V6WLthATX%2BbK2l2nbM9CWzZ7fZ8DTMCPKjwluNOpScoUBwI41qhp%2B9XWw3Ju5Wac%2FClN8UuNKxnuI5EdxqwNQ7dNaXyxzLPNbtgjTGS05uMEK3T2caq%2BpxsIFOUXGz0tkdnXhGsrDcLWsMtK4AToycpPetHV5xV76fvtov0FM6zXGNOjq5LZWFescx6a%2FPeshYb3d7DNEyzXGTAfBzvMrIz5xyPprjoQfC6JCPK%2FQsGlauaH8I%2B8Q%2BjjartrdxZGAZMbyHR3lPI%2FdV46M2m6M1WlKbVeWRIPOM%2BeidHoPP0Uh0bm%2BUwOBUypXAVkVzmoKSUpShCrx2yXQurIiLIKj2dtSfR8SRDt7jchstqLmQD2VnK8dwuEWAlKpTm4FnA4Zry%2BH9P4mrmOXzPz5qu0wvLhS9dYy%2B2lN0Q2hTym%2BjJPAZzXfbblDn7%2Firu%2FufC4EYri9SHItqkSGiAttBKc9tbGScbJxXF%2F4mV%2FZQFgrBHRzSh8ec%2BoK77VpduBcG5aZa3C38kpAzXh0rf7hPvCY0haFNlBOAnFTAkAGsXVa%2FVZLRkQR1R%2FqulxPleK%2FfqSZ9Cr2VTal8KnupLtJu873Bs%2FlAnD7oPDHWM9ntr6ToGCUDfmSN7HHGMVS3OHLtpwcYWGdX8WlOs%2BFXS11ntmqv97Wvol%2BypOdnttP88lesV7LBo6FZ7mmczJfWtKSkJXjHGka%2FwCn8uDIZI8CgfukiN%2FK17tb8NJ3L6A1RS11ae0HUHTb2m7W34zMk%2BQ5u8dwHq8%2FsrAp2ZXVaAVXCMgkcU7pOO6r25x5M7IHoC%2BIopGSHSH8HwoItdXHs%2FkKjbO2pSQFFptxYB5HBJqLHZbdD%2FSUX6iqnemrCu3aTTZZTwWdxSFLQMfCzyzTNLgZGPI5z210l4kMjHkkKG6e2lT7lfIdvctsVCZDoQVJcUSnNVP4VmhU2i%2FI1dbmNyHcVbstKRwQ%2FwDO7t721eFn2b2u23SPPamSlrYcC0hWMEj0VIdaafhan0xOsU9AUzLaKM44oV8lQ7wcGvQa33EYPrmyrOO2biRKe1%2BftKz190dqO0XmZbH7PPcciuqbK24y1JWAeCgQMEEcaxU6BOglAmwpMUr%2BD0zSkb3myONbYIPhSohealKV1cTqrlJKVBQJChxBBwR6a4pQhTvRu1vXOmNxqJeFy4qeHi8wdKnHYCeI9dbCbF9snv8ALsqyyLE7EmoZLy3Wl77OBw454itQOVbZ%2BChpA2bRTuoJTW7Lu6gpGRxSyn4PrOT6qRK1oFpjCbV0UpSqycmaj2sYMqYywIrJdKVEqAIGOFYhnVFxU%2B2hQYwpQB8k9tTZHwa87FmYm%2FxnxMJrq1OiwqOaLgTYRk%2BNsFrfxu5I41IJDLUhhbLqAptYwoHrFdlQLX1xnRLwluNLdaR0QOEqwM1OT0NJghtFzR1%2FNRc6%2BypbCs9thP8ATxoqG3AMbw7KjuqL4%2FNle4Vl8t5fkuuJ5JHWM%2B01DnL3diCk3GTg8D5dTzZ7b4zFkanJTvPyU7y1niefLzVnYmwbsv8ALYzfTb5P7fp%2B6hys0FkNM2SPZ4XRo8t9fF1zrUf3Vxqq9osVuTLWwp4FYRhJAPGszyqF7XDjTbf%2BYT%2BNbuSPZYbvR64jpceeLSQvCdpkcc7W99oK8V02ivTIpi22AtmU6QhC1KBxnhw76r9a67LOr%2BGoXH%2BcI9teRj3ObKeBd0VmHLeTVq4NC6WRZ2TMmHprk8MuOE53M9Q%2FE1k7hqSyW6UqLNuLLLyQCpCjxGeVZYcqoja7%2FHiUP8Nv%2FTXqsmQa7HHpBWsmb20QLQrZ9%2BemP75jfWr22m%2B2q6uLbt01qQtsZUEHkK1tSkf%2FAIVY2wofwxcfoE%2F6qXhbKWeQNc0UVRxtm6aUMI8q3ax99vNvssQSbi%2F0LSlBIVgnj6KyPVUH2yR35Gm2UR2XHVeMJOEJJOMGtk9DpaWVI6KJz2iyFlbXrPT1yntwok3pH3ThCejIz66o%2FwANP43pf9iT%2FwBlSDZ1b57OsoDjsKQ2kKVlSmyAOB668nhaabv1%2Fk6dVZbTLnhhMjpegb3tzO5jPnwaZDdjkqeuypcqEukFG1rHSstftN36woaXerTLgJeJS0X2ynfI54rE1eBB8K2lKUoXFK9lGkJGtNaw7M2lXi290stwDghpPwvXyHnreqDGZhw2YkZsNsstpbbQBwSkDAFaV7AdZNaN2gMSZi9y3TE%2BLSj8wE%2BSv0HHozW67DjbzSHGlpW2tIUlSTkKB5EVUmvknR%2BF90pSlJiqiNveOM5Sr9InqPbVrI4p9FfO4j5o9VcPvNMNlx5xDaBzUo4Fef0mlbqWPHO77%2Byk51r7xVabTFgX5IJ%2FkR7TViRpsSSopjyWnVJ4kIWDiviTb4UlzpJERh1eMZWgE1a2uF%2FiON6THAd%2BUtwsUqQWsZ5j11bugznSVvPV0f4mvYbNajzt8X7IVyqbaraBFXJixd0cGyoJwPNWfqNMdbIZHvBsUoMbwJJK9%2BagO2GdH9y2Lcle9JW6FhA4nAzWW1TrG22y3FyJIalyV%2BS022re49px1Vi9EabkPSzqO%2F5dmvHeabWPgDtI7ewdVXs2X3I9tF3fk%2FAH%2FqhI7n%2BBqq9cKf8A2KT9kr91dlnhTheYRVCkhIkIyS0rhxrYVZbQMqKUjtPCvjpo5%2FlGvrCqEf07HG4Hmq3sBd8l2j4NURtawdcyyCD5DY%2B6rI17q9uyxhEgESLk%2FwAGkJGd3Pyj%2BArG6S0FHcjLn6mb8cnSTvqStR%2FJ5%2FGtPLZ7keiz47UM0HJ%2Fgx%2Bfk%2FAVQAVYuwv9b3H6BP8Aqqce8XSv90M%2Bs%2Fvr3WbT1oszrjtthNx1uDdUU54gdVdxcAwuBKqYmrlhmEjiKC7NQ3mHY7f47OLgZCgnKE7xye6sVY9bWS8XJECGZBfWCUhTRA4d9YTa1cmpUVrTsNKpNwecSsNtjJSB299YLZtpy%2BwNWx5c22PsMpQsFa8YGR561Q3pTnz5xltiiFt6v9P%2BVboSCOI419YwOFcp5V0zfib30avYaitsClr54ZykuW3Te4oLxIezunOPJFa28esYq2th%2BttOaW1Lfn9XLefZf8iOFMF%2FCg4ongeXCoDr%2B4wLtrW73K1giFJlKcYyjc8k8vJ6qtxgj8KS7vtYOlKU1QTqP31ux4O0G5QNk1oRdJDzrryS62l05LTaj5CR3Y9taTjhW1vg2bUZGqEOaYvKGkz4bAVGdbTuh1pOARgciOFJmFtTIyLV3UpSqqclYHXMWRM086xFZU86VpIQnnzrPVxikZMAnidEfBFIIUF2cWu4QLjLXMiOMJU0AkqHM5qd1wBiuaVg4TMOERMNgLgFClx11Tu1xQGrFZx%2BgR%2BNXFiolqjQ8S%2FXPx96a%2ByooCN1AGOHnqvt8STKx%2FTj82kZMbpGU1VpoBDbusLe24hKklwnBHDIBxV8J4JqFWHZ7CtN3YuLVwkuKZJISpIwamw4Cl6bCkxIS2TySo4kTo2kOUP2vFQ0RJ3SQekb5HHyqo3pHB%2FKOfXNXntbQtzRUhLaFLPSN8EjJ%2BFVIiJK4%2Fmz%2FwBmarbKJ7sgEeKWNt3PEor7Kb7FYUeXf5UiQ2HXIzSVNFXHdJOM1cnVVT7D2HmrtcS4y4gFlHFSSOs1bHVWtgs4QgLR1YPtwa7VZ3naXKgXeXBTa2nAw8psKLh44668EnancHI622bay26oYSvfJ3T24qI6v4aquv8Aml%2B2sWj4Q89X4YnOPa8pk7nKbI5of1df1V3aA0wLc2btcF%2BM3OUN9bqjndB6hUxry239Xxj%2FAISPZXqqBXtcWJsUQa0Ly3G4Qbcx09wlx4jWd0LecCE57MmsVL1ZphUR5I1DacltWPztHYe%2Bq68LxIVsuaBAI90WuYz1KrURaG9w%2Fk0cvmimRxchaa59GlkZsSWqdJUmJIUkvLIIaUQQVHjyryutOtHDrTjZIyAtJTn11%2BgGmI0c6athLDRJhs%2FIHzBWt3hittt6ztAbQhA8QPBKQPlmmsk5GlBzABao2lKU5LSrh8Ei3SpG09dwabJjQ4TnTL6gV4CRVPVtr4Ise3I2ZOPxgjxx2a4JZHwsjG6D3YpUppqkztyualKVUVhKUpQhKUpQhKVxnnVH7RL5eY2sp7EW6TGGkKAShDpAHDsqnmZjcVge4Wq%2BTkNx2cnK8aVANjM%2BdPtM5c6W9JUl4BJcWVEDFT6nwSiaMPHypwyiVgePlCkKTggEd4r46Jv%2BrT9WottWmSoWk1vw5DjDvTIG%2B2rBxmqh98moD%2FTM77Y10vp1Us7N2seK%2Fg5pK2HQhIJISB5hX2c4qidI369P6ntrL11mONrkJCkqdJBHYavb5NMpO1%2BezNYXMFUq4u%2BzRU%2B6yp3uoGxIdLm70WcZ6udeUbKVBQ%2FhgfY%2F%2Bald61rY7RcVwZjroeQAVBLZI41mrLcY11trU%2BGpSmXRlJIwafylY2%2FhUhrtbPKQAC757XbFb6CM2yVZ3EBOe3Art30%2FOFRTaw86zouS4y4pte%2BjyknB%2BEKpU3K4f22T9oavYOrdmMLw6lW2%2FwBRx6uUQlhPSuvahouHrzTibJMnPw20vpe6RlKSrIzw4%2BeqwPgyWAgj3zXXj%2FhN%2FurM7G5cp7VLqHpLzifFVHClkj4SauLqqrlwOxJDHdrS1OwbsscThtLz2yMmHb48JKitLDSGwo8yEgDP3VrD4ZH8dbP%2FAJA%2F6zV8602jaS0fcGoF%2FuRiSHm%2BkQnoVKynOM5ArWjwlNYWDWGprbN0%2FN8aZYiFtxRbUjCt4nHHupMIPK1oPIpVTSuN5Pzh665q2kpU92J7RJOgdSF1wLftMvCJrCeYHU4kfOH3ioFSuFocKK6DRX6H2a5QrvbI9yt0luTEkIDjTqDkKBpWvvgc6klLN20s%2B4pbDSBLjZP6PJwtI7jwPrpVF7eJpWGmxa2OpmlcEcDXF1AQa5qo9rV8u9v1QliDcZMZrxdKtxteBnJ41DvfVqU%2F05O%2B0rGm3McUpjLTYWdNso4nFpHhXLrrVEXTkHPB2a6MMMg8Se091RGxaAk35ly8ailvtSpSt8ITgEDv7PNXj2VQk6gv8m53l52a%2FFSkt9Kre49RPmq4AMU6Fnvf4kg%2FD8BETRmD1H%2Fl%2BAsFo7TUbTcV%2BPFfddS6sLJc6uGKz1cV8OuttNqccUEoSMqJOABWiyNrBxb4V1rWxtoeAohtjGdGOfTI9tUkeyrNvc%2BZry9e41pJbtTCt558jgrHX%2B4V607KYOP1rI%2BoKY1rQbK8pssWbYSl%2BOLA6tV%2For%2BNtrH%2FALlNbEdVQGz7Noduukacm5PuKYcCwkoGDip91VOVzTXFaWiwZsSNzZfJKqvXujL7dtUSJ0JlpTC0pCSXMHgONTnQ1vk2vS8OBMSlL7SSFBJyOZrMkhKSTyFReRr7S7CXR7pJU4jIKEoVkkdQ4U7nNOwRtF19lNuLh6%2Bd2S99F33P9l5tsDradFvoUtIUtxASCeJ8rqqkMjtFWvYLZM1neBfr2hSLa0fzWMeSu893tqbiwWXGPcuJ9kK1cXPZrmekRyPk18fovPbDSy72X3LSGtqhfk%2Fqqq2KY99r3EfFVf6hV0jlXgiWy3Q3i5Ehx2XCMFSEAHHZXv4YrKz8oZU3qAUvSaTXO12KIHOuiVq54ZqcavsKs84Kx6l1XOxSBCum1KxQLjFZlxHpBS6y6neSsbiuYqx%2FDOUDq2wDPEQXMj%2FrqndHX6VpjUsK%2FQm2nZMNZW2h3O6Tgjjjz1xgJj6Wg78y3G1Ls60Kxpy5Ps6Ts7bjcR1SFCMkFJCTgitIxyq5Lj4RGrptvkQnbXaUofaU0opSvICgQevvqm67E1zbtDyD4SlKs%2FY1shu%2BtZjVwuLTsGwpUCt5Qwp8fNbH%2FdU3ODR2ogE%2BFYPgc6akss3XVb7aksyEiLGJ%2BWAcrUO7OB6KVf8AZ7bDtFtj263R0R4kdsNtNIGAlIpVJzi42ntFBeylK47a4pKkttf8cEf5VHtNQkCrv1joRrUd3FwVPXHIaDe6GweRPH76ww2Ssf3w59kK85PrJZJ3PA6K89mYE8krnNHRXm2EfGbp%2Bwj2mrWqK6H0gjTLslaJi5PThIwUYxjNSs8q28WIxRBh%2BFq4ET4oAx%2FlYHXcyRA0nPlxXVNPob8haeYOapaVqS%2FXFkwpV0kOMuqCVJJ55NXnqW1pvNkk21TxaDycb4Gccag7WylhDiF%2B67nkqBx0Q6jVtlfKytviZc8g9H8vz2prpezwrLaWokNvAwCtR5rPWTWWA4V8tJ3EBPPAAr7qJNrdiYGMDQKpMUpTqriYup4ZbVjmQa14nWO8qmyFJtU0guKwegV2nurYvqrjdFXsHPdiE8RdrE3Okj2gaHurisbpltTVggtrQUKQwgFJGCDjsrsvalos8xxtRStLKykjnnB417sUICkkEZBGCDVPnbuRWoIai9MH4pUjs9u94k6ugMyJ8txpSlbyVqJB4Gru5V0NxIzat9uMyhQ5EIANd%2FVVnMyRkvDmt49KhqNfJgRFj387N2tU%2FDEfDm0C2MZH5G3%2B1Z%2FdVJVanhUzEytr0ppJ%2BLRGWj58E%2FjUF0bpa96tvKLVY4a5Dx4rXyQ0n5yj1Cus6YFfcLKwvVmptojZXrTVu47b7UtiIr%2BdSvybeO0Z4q9ArYvZbsO05pZLU67IbvN3GD0jqcstH%2FkQfaatlCEpSEpAAHIAYApbp%2F8AapNj%2B6pnZxsA07YlNzdQui9zk4IQpO7HQe5PNXp9VXI0y202lttCUIQAEpSMAAdQFfY4UpBcT5TAAPCUpSuLqUpShCUpShCUpShCUpShCUpShCUpShCUpShCUpShCUpXivkwW%2BzzJx%2FkGFuDvIBwPXQhagahsFz2lbeb3BtWN1U1SXJBGUMtIwnfPq4DrNbUbP8ARtl0XYEWmzx90AAvPKH5R5fWpR%2FDqrC7E9Fo0rpbp5LaTd7osy57mMkKWSoIz2Jz66nwqbn30otbSClKVBSSlKUISlKUISlKUISlKUISlKUISlKUISlKUISlKUISlKUISlKUISuidFblxyw7koUoFQ7cHOPNSlCF3gY5UpShCUpShCUpShCUpShC%2F9k%3D&logoColor=white&logoSize=auto&labelColor=white&color=%23AF001E" style="width: auto; height: 25px;"></a>   <a href="https://github.com/vita-epfl/ToSS"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Code%20(link)-gray?style=flat&logo=GitHub&logoColor=black&logoSize=auto&labelColor=white" style="width: auto; height: 25px;"></a> <a href="https://github.com/vita-epfl/TIC-TAC"><img alt="Presentation" src="https://img.shields.io/badge/Presentation%20(link)%20-%20white?style=flat&logo=googleslides&logoColor=white&logoSize=auto&color=%23C78C06" style="width: auto; height: 25px;"></a><br>

<hr style="border: 1px solid gray;">
<br><br>


## Problem Statement

In our [previous work](https://deep-regression.github.io/research/tic-tac), we addressed the challenge of unsupervised covariance estimation through better parameterization (TIC) of the covariance. However, TIC requires significant computational resources as computing the hessian is expensive. While there can be multiple approaches to mitigate this, such as using just the gradient or utilizing smaller models, the inherent challenges still remain.

These challenges stems from a key limitation of deep heteroscedastic regression: estimating sample-dependent covariance in an unsupervised manner. Without labels, the covariance estimator solely relies on patterns in the residuals across various samples and may be inaccurate. Therefore, can we use self-supervision to improve covariance estimation? Specifically, we ask: 
1. How to supervise covariance estimation when annotations are available?
1. How to generate pseudo-labels when annotations are not available?

<br><br>

## Supervision

To gain intuition, we propose studying the simple task of learning a bivariate normal distribution, as shown below. Given samples from the unknown true distribution, how well do different supervision objectives optimize the predicted distribution to match the true distribution?
<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/setup.png?raw=true" alt="setup" style="width: 25%; height: auto;">

<br>

#### KL Divergence

We first turn to the KL divergence for supervising the learning of the covariance, which is a popular measure to quantify the difference between two distributions. Moreover, the KL divergence gives rise to popular machine learning objectives such as the cross entropy and negative log-likelihood. The KL divergence between two gaussian distributions $p$ and $q$ is defined as
<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/KL.png?raw=true" alt="KL-simple" style="width: 70%; height: auto;">
An astute reader may notice that the above fomulation is not very helpful for regression. This is because the mean and covariance are unknown for the target distribution. Instead, we rely on *i.i.d.* samples $(x_i, y_i)$ to supervise the covariance. We therefore ask, how can the KL Divergence be formulated for deep heteroscedastic
regression? 

A logical approach would be to replace each label with a distribution. Specifically, for a sample $xi, yi$ from the dataset, the pseudo target distribution can be set to $\mathcal{N}(yi, \Sigma^{(\texttt{prior})}_Y (X))$. However, this approach requires calibrating the KL Divergence since the optimal value for the covariance is not the same as the prior! This can be seen through a simple setting in Lemma 1.

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/lemma1.png?raw=true" alt="Lemma 1" style="width: 80%; height: auto;">

So what does this lemma imply? If we swap out $(x_i, y_i)$ with $(x_i, \mathcal{N}(yi, \Sigma^{(\texttt{prior})}_Y (X)))$, *the predicted covariance is twice as much as the true covariance*. This also motivates the need for calibrating the KL divergence such that the resulting optimal value is the same as the true covariance.

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/calibratedKL.png?raw=true" alt="calibrated KL" style="width: 70%; height: auto;">

With this formulation, $\widehat{\Sigma}_Y(x) \approx \Sigma_Y(x)$. Moreover, this solution truly allows the KL Divergence to act as a regularizer over the covariance. When the target covariance is unknown and cannot be set as the prior, the calibrated formulation gives the optimal solution $\widehat{\Sigma}_Y(x) \approx \dfrac{\Sigma^{(\texttt{prior})}_Y (X) + \Sigma_Y(x)}{2}$. We can observe this in the graphic below. Unlike the negative log-likelihood which shows significant fluctuations, the KL divergence demonstrates stability in the predicted covariance. This is because the prior anchors the predicted covariance, preventing disruptions. 

<video class="responsive-video" controls loop autoplay muted>
  <source src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/videos/toss/homoscedastic.mp4?raw=true" type="video/mp4">
  Your browser does not support the video tag.
</video>

However, we observe that a *residual covariance* across both, the negative log-likelihood and the KL divergence.
Why does this happen? Our solution in Lemma 1 is reached only when the mean estimator has converged to the true value, and when exposed to multiple targets $y_i$ for the same $x$. However, this may not hold true practically because 
1. Samples in a batch are *i.i.d* and it is unlikely that the same observation with different targets are there in the batch.
1. The mean estimator may not have converged. Moreover, convergence is not uniform across the dataset!

In practice, the predicted covariance is heavily dependent on the difference (residual) between the prediction and the target. Specifically, the optimal solution is:
<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/residualterm.png?raw=true" alt="Residual term" style="width: 50%; height: auto;">

If this residual is large, it dominates the uncertainty estimate, pushing the model toward learning something that looks more like an error-driven "pseudo-covariance" than the true underlying covariance.

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/residualcov.png?raw=true" alt="Residual covariance" style="width: 100%; height: auto;">

Details! The model essentially aligns the covariance with the error direction (the line between prediction and true value).
This slows down optimization because now, the residual affects how the mean is learned. The larger the residual, the more it overpowers prior knowledge about the covariance, making updates less stable. While the negative log-likelihood fails, even the KL divergence is ineffective because it gets overwhelmed by the residuals, leading to unstable updates, especially with higher learning rates.

Because KL Divergence inherits the same weaknesses as the standard negative log-likelihood (NLL), can we use the 2-Wasserstein distance as a better way to guide covariance learning? Intuitively, the 2-Wasserstein distance does not rely on the residual, making it much more stable. Moreover, it allows for a mechanism to directly supervise the covariance.

<br>

#### 2-Wasserstein Distance

The 2-Wasserstein distance measures how different two probability distributions are by considering both their mean differences and covariance structures. It provides a more stable way to compare distributions compared to KL divergence, as it captures overall shape differences rather than just pointwise mismatches. For two multivariate normal distributions, the 2-Wasserstein distance is defined as 
<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/wass-eqn.png?raw=true" alt="Wasserstein Equation" style="width: 50%; height: auto;">

This formulation, however, requires computing the root of a matrix, which typically involves eigendecomposition. Unfortunately, the eigendecomposition in popular deep learning frameworks can potentially lead to unstable gradients. In fact, if the two distributions are commutative, then $\mathcal{W}_2(\mathcal{N}_1, \mathcal{N}_2) = \parallel \mu_1 - \mu_2 \parallel^2 + \parallel \Sigma_1^{1/2} - \Sigma_2^{1/2} \parallel ^2_F$. But what does it mean for two distributions to be commutative? When two matrices commute, it means that $AB=BA$, which implies that applying one transformation first and then the other gives the same result as applying them in the reverse order. Intuitively, it means that the two covariance matrices share the same eigenvectors, and transform the data along the same axes. What might differ is the degree of transformation, which corresponds to different eigenvectors. However, assuming commutativity just to avoid eigendecomposition is a very strong assumption. It essentially means that the structure of the covariance is known a-priori! Is it still possible to avoid eigendecomposition for non-commutative matrices? With theorem 1, we show that $\mathcal{W}_2(\mathcal{N}_1, \mathcal{N}_2) \leq \parallel \mu_1 - \mu_2 \parallel^2 + \parallel \Sigma_1^{1/2} - \Sigma_2^{1/2} \parallel ^2_F$ for any set of covariance matrices!

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/theorem1.png?raw=true" alt="Theorem 1" style="width: 80%; height: auto;">

Theorem 1 is significant from a practical viewpoint. The bound allows us to extend the simplification for the case of commutative matrices to the more general case of non-commutative matrices. By doing so, we remove the eigendecomposition and make the optimization more stable. Finally, reducing this bound also reduces the true 2-Wasserstien distance between two distributions!

So how does the 2-Wasserstein compare with the KL Divergence? We study this through our toy example:

<video class="responsive-video" controls loop autoplay muted>
  <source src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/videos/toss/homoscedastic-full.mp4?raw=true" type="video/mp4">
  Your browser does not support the video tag.
</video>

We make two key observations: at higher learning rates, the negative log-likelihood and the KL divergence suffer from unstable optimization. This happens samples not aligned with respect to the predicted covariance tend to destabilize it, since these samples are considered *very far* from the true distribution. In contrast, the 2-Wasserstein distance allows for smoother convergence since it does not depend on residuals. The 2-Wasserstein benefits from direct supervision of the covariance. Moreover, if the prior covariance is reasonably close to the true covariance, we also get lower likelihood values!

<br><br>

## Towards Self-Supervision

While we have studied objectives for supervision, we still need to find labels for the covariance! Such labels can often come from good prior knowledge about the task being solved. However without this prior, we need to find signals for the covariance within the data. We do this by looking at nearby examples and using their covariance as a proxy for the unknown true covariance. By doing so, we capture two key intuitions:

1. The target has a high (co-)variance if it exhibits large variations in a small neighborhood of the input.
2. The closer another input is to our input, the likelier it is that the corresponding target is a potential label for our input.

We describe our algorithm and input below.

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/pseudolabel.png?raw=true" alt="Pseudo Label" style="width: 80%; height: auto;">

Here’s how it works:

1. *Find Similar Data Points (Neighborhood Selection)*: For each input $x$, we find other similar inputs in the dataset. The similarity is measured using Mahalanobis distance, which takes into account both distance and spread (instead of just Euclidean distance). Finally, we interpret these distances probabilistically through the *softmax* operation. Neighbors with smaller distances are much likely to be neighbors in comparison to samples with larger distances. 

2. *Compute the Variation in Their Outputs*: If an input has multiple similar neighbors with very different outputs, it suggests high variability. If all nearby points produce similar outputs, the model has lower variance in its prediction. Moreover, different neighbors contribute to different degrees. We use the probabilistic interpretation of neighbors to compute the *`expected'* covariance for out input sample.

Why does this work? The network spends a significant amount of time trying to identify patterns from just the residuals. This may not even converge to a reasonable value! By explicitly encoding patterns within the dataset, we provide a much stronger signal to supervise the covariance.

We now have all the ingredients needed for self-supervision! For each sample, we obtain a pseudo-label for the covariance, which is trained using the 2-Wasserstein distance upper bound.


<br><br>

## Experiments

Does using self-supervision truly retain accuracy while being significantly cheaper computationally? We study this through a similar setup as TIC-TAC. We conduct experiments across real and synthetic datasets, spanning univariate and multivariate analysis.

<details>
  <summary> <strong>Univariate</strong> </summary>

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/univariate.png?raw=true" alt="ToSS univariate" style="width: 80%; height: auto;">


We learn constant and varying amplitude sinusoidal with heteroscedastic noise. We observe that self-supervision converges much faster, fitting the sinsusoidals in a smaller number of epochs. In contrast, while TIC did fit the sinusoidals, it takes significantly more number of epochs to converge.

</details>

<br><br>

<details>
  <summary> <strong>Multivariate</strong> </summary>

  <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/multivariate.png?raw=true" alt="Multivariate" style="width: 80%; height: auto;">
 
We re-use the same setup as TIC-TAC for our multivariate experiments. We compare different methods simulating increasing dimensionality of the data. Our quantitative results highlight two things: not only does the 2-Wasserstein bound have better accuracy of the mean, it also learns the covariance accurately in fewer epochs when compared to baseline methods. Moreover, the 2-Wasserstein bound also performs better in comparison to the original 2-Wasserstein distance between non-commutative covariance matrices.

  <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/multivariate-compute.png?raw=true" alt="Multivariate-compute" style="width: 80%; height: auto;">

Finally, we compare the compute time and memory requirements across all the methods. We observe that the 2-Wasserstein distance retains accuracy in comparison to the state-of-the-art while being computationally cheaper.

</details>

<br><br>

<details>
    <summary> <strong>UCI Regression</strong> </summary>

    <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/uci.png?raw=true" alt="TIC univariate" style="width: 199%; height: auto;">

    We conduct experiments on datasets from the UCI Regression repository, and show that our analysis from the synthetic examples also translate to real world datasets. Not only is the 2-Wasserstein accurate, but also computationally cheaper. Results with standard deviation are available in the appendix.
</details>

<br><br>

<details>
    <summary> <strong>2D Human Pose Estimation</strong> </summary>

    <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/toss/humanpose.png?raw=true" alt="Human Pose results" style="width: 80%; height: auto;">

    In this experiment, we don’t highlight self-supervision for its computational efficiency. Instead, we showcase its potential in a hybrid training setup to push the boundaries of state-of-the-art methods. Our initial attempts at self-supervised learning didn’t quite match the performance of TIC. We suspect this is due to the pseudo-labels being inaccurate, since they were derived from a low-dimensional representation of the input images.

    However, this led us to an alternative approach: a hybrid training paradigm. By pre-training with self-supervision and then transitioning to TIC (trained using the negative log-likelihood), we observed significant advantages—preserving the benefits of both the 2-Wasserstein bound and NLL-TIC.

    As illustrated, we first train our models using self-supervision for 20 epochs with the TIC parameterization. After that, we switch to the negative log-likelihood, which allows greater flexibility in optimizing the covariance. The results show that the hybrid approach outperforms standalone methods, achieving both low mean square error and low negative log-likelihood.

    This experiment underscores the power of combining different training strategies rather than relying solely on one. Hybrid training could be a promising direction for further improving deep learning models.
</details>

<br><br>

## Conclusion

Our study is best concluded by the following points:

🔹 Traditional methods struggle to estimate covariance accurately without supervision. <br>
🔹 We show how the KL divergence can be calibrated for regularization, but noted its sensitive to residuals.<br>
🔹 The 2-Wasserstein bound provides a stable way to optimize covariance estimation, avoiding the pitfalls of KL divergence and NLL.<br>
🔹 Our simple neighborhood-based heuristic generates effective pseudo-labels, enabling self-supervised learning.<br>
🔹 The result? A computationally efficient approach that improves both accuracy and convergence in deep heteroscedastic regression!<br>

<br><br>
## Acknowledgement

We thank the reviewers, for their valuable comments and insights. We also thank [Reyhaneh Hosseininejad](https://www.linkedin.com/in/reyhaneh-hosseininejad-a2b54b138) for her help in preparing the paper.

This research is funded by the Swiss National Science Foun- dation (SNSF) through the project *Narratives from the Long Tail: Transforming Access to Audiovisual Archives (Grant: CRSII5 198632)*. The project description is available on: [https://www.futurecinema.live/project/](https://www.futurecinema.live/project/)

<br><br>

## Citation

If our work is useful, please consider citing the accompanying paper and starring our code on GitHub!

```
@inproceedings{
shukla2025towards,
title={Towards Self-Supervised Covariance Estimation in Deep Heteroscedastic Regression},
author={Megh Shukla and Aziz Shameem and Mathieu Salzmann and Alexandre Alahi},
booktitle={The Thirteenth International Conference on Learning Representations},
year={2025},
url={https://openreview.net/forum?id=Q1kPHLUbhi}
}
```
<br>