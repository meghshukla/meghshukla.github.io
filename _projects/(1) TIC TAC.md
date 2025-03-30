---
name: "TIC-TAC: A Framework for Improved Covariance Estimation in Deep Heteroscedastic Regression"
slug: tic-tac
tools: [Method]
image: https://raw.githubusercontent.com/deep-regression/deep-regression.github.io/master/files/images/tictac/tic-tac.jpg
description: '<img src="https://icml.cc/media/Press/ICML-logo.svg" alt="ICML Logo" style="width: 100px; height: auto;">'
---

<style>
.responsive-video {
  width: 100%;
  height: auto;
  max-width: 100%;
}
</style>


# TIC-TAC: A Framework for Improved Covariance Estimation in Deep Heteroscedastic Regression
<br><br>
<span style="font-size:20px;">**Megh Shukla**, Mathieu Salzmann, Alexandre Alahi <br>
*International Conference on Machine Learning (ICML) 2024, Vienna*</span>


<a href="https://openreview.net/forum?id=zdNTiTs5gU"><img alt="OpenReview" src="https://img.shields.io/badge/ICML%202024-OpenReview%20(link)-black?style=flat&logo=data%3Aimage%2Fjpeg%3Bbase64%2C%2F9j%2F4AAQSkZJRgABAQAAAQABAAD%2F2wBDAAMCAgMCAgMDAwMEAwMEBQgFBQQEBQoHBwYIDAoMDAsKCwsNDhIQDQ4RDgsLEBYQERMUFRUVDA8XGBYUGBIUFRT%2F2wBDAQMEBAUEBQkFBQkUDQsNFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBQUFBT%2FwgARCADIAMgDASIAAhEBAxEB%2F8QAHQABAAEEAwEAAAAAAAAAAAAAAAgBAgYHAwQFCf%2FEABsBAQEAAwEBAQAAAAAAAAAAAAABAgUGAwQH%2F9oADAMBAAIQAxAAAAGVCgUcEc7q3s%2Be6264LLrZOjonLIZXLZ%2BHeCl5rONXsZhri0kvu35%2B%2Bkn0TrHmQacl1twBRQnWjhIuL%2Bu6%2FwArI8K97X9vLK%2Fpaz6P8Y2w05X6fPnhpNjUPy%2B2hW9%2BjMtLyFj9OMxWNH0AhSavouWkh48E%2BkvJrbZLEDyrtRdjjei29HaRdnUfFE%2FIpFcnntfEhlM6GPW8NwUV6HW70kJHqQ3Fbh0%2B51Pi%2BmAWZYbj%2BWW%2FdL%2BUXcPq5d76Q8UqbRmt82%2FoenrKE0f2NqcvF9F27sbxbdc3sxrSnljl0MZgdXp%2FCH6XDf8Ay6%2BkHpyNfO7Ce%2FnwW6%2Fl7dLxLrFupt6UBAKk%2FYYJiNRkm1CWX7HdC4nHW6mMwfD8ww7gfmDT4ZZneB533v03W1puvXR8S5ZRMWrL%2BwYPdm%2FWrZ0qIZSUTOoOyph6YnUZJdxDl0m71pjdSrGYNh%2B1vI5bz1%2FXPmvx8zpZrCrqfXdFYstjntLX3nelb9CO51%2B0xt8n2fKPnx0%2B%2FwCcpUtKg3Hpupt5rsfQ4rMKBaVWl0DJiwqtxpRMq%2Bl5vbr6KdnXnqPPMPL8Tx1hZ0efrsgAFK0NmM7EowxApbcId6bkhG5ahVKi2%2B0FQAABQ7BL5nhMoCALa2GJRamp1T5zcfteIyqAAAAClVDJ9r96TSWryXgAUqHFy2EF8BkbHJQUAAAEUVJY74wzM0AAAAW3WmIwS%2BjWmFiAUWoAAFFVbNwydjH3uW25AAAAFl4ts5bTV0RfoViqwCZ3gxbUZKVvSzZWZSkTG8rXJbcAAAAAC0APIi4Gp%2FNGeSb9GO%2FOQTkqAAH%2FxAAwEAAABQIDBgUFAAMAAAAAAAABAgMEBQAGBxARFBUgITAxEhYzNUETFyIyNCM2QP%2FaAAgBAQABBQLLXoO3iLFvMYppJHeYhzDsF5t04oyp1KKYSihLOW4sb%2FmGQx2LBQCNuBjKlrWg4jLFKO0FoqoGEMxrEg%2Fhga558stQr8aZSLqPUtHEUHIgcDBwrm8KVzSK29tvWqBlFyPijrWta5YkDpBZdq%2BbUw%2FbykeOF0WIXFEbmkchqx772YhRAQ4Hfo3J71UL%2FeZYrdFziAzQW%2B47OhxHZUqqzvmJNhU78X2qe08wwkEG6iZkD2R7FWIv%2Bx1rrQaalN4Asi4RnYzLeCFEeJKGXJ407khnZ5fcr6oGCebfN8odx%2FTXesLvUyeBq0n%2BUvAX47g2o4rONJOSWlXVpWJv9vc%2BHgRDKu9YfTG7JwBy8Q%2BFBUxFQoyRT1sxKBICVPezr%2F0ZYXepk8%2Fkn%2Fd88OZ5qjG31cDQIbIihkjRrsHzShpuT6hy8gr5Gp0PFEuQ0c5YXEHXJ%2BoCbKZVKtKjyHMQ5Z4eOdqtit3o0RmknUq9O1LvZet7L1vZxUY7M9pa0GC6nkmOCvJkfV1OQtGGNd0ocfNkpS9yyThMfyrX8sOoZCVkfLMXoNrxYhdMenGy%2BeFqmtv5z%2Fcf25V2qB9WvmsVPb8uWWugYUf2ftlfnK4OWeFnKEznq1rTKAH%2FACBnir7ZpqLe1pB0TybJFrybJU5td%2B2Sw9nm8I%2BJeUb4TXnGkq55MkvKZDWFw6wmc9wQH73FejS3Vvu0jX3bbhV4XmNzGjQ1kWpQTQDKW%2FKLeh4XOo8POravgluwyeJEoL3J2xI7AYFCtwoVuFCmceRnV7LGWnc433Bv6GUr7Y%2F5u%2BLSodrtb7jvH37OM9xb%2BhlKe2P%2FAOvjw9aC5uXh1qQuhjGqXE8I%2FmO%2BbNUEXkdeMas3C6o0a81RtTF2xxY1dT6q3HhOz8a3ANCGoYpt9nnq7D1u9YZsdkheLF5oYVuYVyAM9RyHmXnpxoJCu4tpDZoHiuaDLPRq%2BHUwiooQUjdTSoW33M6e1sO35ZIhATLwDXxTgNUJlHZpLq4Spc%2BiYuoX032W6OnpQ1hOh9ON6PasV4sSn6fz3q0WG74LpXLEhMxD1uLNzoPR%2BKsy1jzzghQIHRHLEK1glWJ%2FwHj%2BR5HiIw0s%2FhIhKIYfPR00yEutXTZDWbSlodxDvA55989dAtmyXc2eCt1rBIaUHU%2Bfmft9vPM7htN5BG11rtWlDzAAMoazrCM9KkkVIgf8MnGIyrS4MNnjNRxGuGZgTEwsbcfSJrXw2BodNIqRBCg4f%2F%2FEACQRAAIBAwMEAwEAAAAAAAAAAAECAAMEERIhMAUQIDEGE0BQ%2F9oACAEDAQE%2FARApb1CjeGeD47QWtVw0v7GituzASqwSfcsVgeBullKeomWN69k%2BVlbrlWpTKS5YtsIAVMo%2BvI9qnUy6aYW3moR01eoKLZ3iLiY8T23jgQYi8bLmBIBj%2BqOUfiz%2BH%2F%2FEACgRAAEDAwIEBwEAAAAAAAAAAAEAAhEDBAUSICEwMUEQExQVMjNRYP%2FaAAgBAgEBPwHZwUKd8yrlxA4KlVcSqNJ1TovR1PxOaWcDyLfMy%2FSVpFZsptuxpkLGAEGUWS1XYioUN9LEQ%2FUn3zLYaChk6axuQZple5N0wFXqeY%2BUBvgQsl80HHUsX9fgEd%2FZXVi6q5DFuBVlRNJsLvzOn8x%2F%2F8QARRAAAgADBAMKCggFBQAAAAAAAQIAAxEEEiExECBBEyIwUWFxkaGx0SMyMzRCcnOBksEFFGKDk6KywiRAUoLiU6Ph8PH%2F2gAIAQEABj8C4J5051ly1zZjQQ0uyS2qPTqCIKmctw7NzWN%2B4PujGM43rjojCcpl%2BzEKtpkTHY0qwoBHgbRLdv6Q4Jjk4ChjOKasxLxW8py5xGOryRgTBxpCvInzJLA%2BgxEJZbd5TINiScIrs1mPJE9L29W7TDkEeN1QAGz5NV%2BK6e0aotFpIY3iKVIwpGEuh477d8GzVvYXvdpzrDWa2zBcUVBNBtgEYjVbmi0%2F2%2FpGhYeY%2FiriYZMTT7MbfgMbfgMT7PLLVpicqY%2F8QbhqvK4jP84h5i3Wuipq4ygo%2BBXZCet8hoan%2BmPnqVG9MLulN2lAK1BSppp8qvTFA4MMInPLkO6NTfAcgjzWZ0QC8h5a8ZEWv1Im%2BsdP0j93%2B7TO9Q9kWjivQJFb0u8WoAvdGEpgePe90GfOa8%2FNDT3mhFFMCDjBtMqapA9EA8UYxjjEsOaSWvFvhOnEmFox6dGIEeKOiMotXqRM9Y6fpD7v92md6h7ItXrajyXa6y3R2xMlq153BX8p03kN1uMQkwZaRTHVtQGO8iaDneOm3tTA3P3aZ5OAuHsi0spqC2egcujOKxXj0yWIob79ujyafCIqstB7oW7TGNnXGyNnXExJgBEGYUoTxKvdHi9S90Yp0KvdBFilohmA76lDgRxc8V%2BtzRzTG7488nfit3xca1zqHPwrd8U28ehmnrfVD4pAOwx5jZ%2FwV7oP8DZ%2Fwl7oaXKrSgNDqIv2m7dSXz6K6JvMNOUSOLf%2FALdOVY4opSJ%2B3EdjaX9QRlTSOdu3UTn1Jvu1LP8A34fDAArWBNSVg2w1im5jrjyY6%2B6Gd5eCipzhxaA1JhzGzAxg56u%2BPKHq74efKUhaU32ovO3bqJz6k33QstlEyYVvUvU%2BXJFPqVfvv8Y80%2F3f8YlKLPuCSq%2BnezpyckWbGvhV7YQAUA02wEYbi3ZExcwDhGWEYRdvYRlTRhG4rK3WbvqG%2FSnVF9pzbljSXve7SA9cOKM36Yzfpjxn6Ya5XHjifeNbrMo%2BIwNNl9qvbC6bX7FuyJvPwCy8ya8BavaN%2Bo6lm9qvbC6bX7F%2ByJvPwEnCq3X%2FAE69ycxvXb2zvi0TJVbpdjj6x1JDnJXBPTCeFuYekVHzjzhPjXvjzhPjXvi1KJwYmUwF1l4ueHfYeAm2iniNT8uvZ6NQfVh%2Bpowig1M4w0ZcCzkeVuv1a9htAQkXSpP%2FAHn0Y56uHBS5YFSWApFgSl0iStR7teZJOEyhummUTP4UtJWp3S%2BvZWLrbOGZLMt9q5YRJtFvk%2FVVlOHpVWvUOWBgBcFGzgJo%2ByYnptFOzhrS%2BxX%2BXBERbUAou9p8A4WkWtqeM6nq4ORalWt8tePuXhcM4siUoxlLe6ODnyaeEK0U8UTZR9BynCTa71Ala4ccUAoBlwkudJKy5kksSW21%2FwDIvHZwGGcY5wsiWwRmri3NCyJQwz4ZpktRJtA2qo32UGRPWjZjGuGvlX5QrEXbNXFwRxwqyZa36YvdoT%2FINJmryg1pjD7pLZrKrXRMCmmXHoz0CAo8btiXarYLiXlZVaqkiLqigH8k1ntCB0bjFaQ0yxqJsn7TAQVnIF5jFBAWRKVjysBC2i3i84ylmjDZCoihVXIDZGet%2F8QAKBAAAgIBAwIGAwEBAAAAAAAAAREAITFBUWEQcSAwgZHR8KGxweHx%2F9oACAEBAAE%2FIehgbzUzvAepJBu4EGbCe5CkFAAtn%2FIG3M2%2BKNbG6EQiSf4g8QFRiEG6wTQNB8cLLQE5uYMPumHt3motbIEN0Jr8J7CPQAZcki8IM5ADqSFxeAgLExt0HeWNB940cIz1MpMm5sRQ2MBoJFoBAAgHO20VMOUaHSJJJ7QWGzxA3fhRWYVg0ATe%2FsA9HsgtIDOkvGGLcRs4hv8AGYpWIAzMoeTGhhzQuFQsHmGA2iMZfQGDyJ3jAoCLcestSBxBhies2Q4hkKKI8DlO%2BhQDl4k4IAwRj2SM94DoK0ACA%2B2FcngAdtDlRSFAsL2nC%2B3EHiyFjASZoHZLg3FNsQwJYnP94YHEoyxAJBTlhElMXHsI27gdSOD0Q4xGZUHxgxRoX8gw%2BvJoXgdPNAVpYmv9JtxC8ofqCCqCXH6lCXyH8CDqQtwAA14Q44UORFNBW1Q580xXC9jxHARbCiOp4hsqwmTuirQGELouMDxHPnKHjBgqDJhllckQrA%2FAmOAHgTeHKffbzXp%2BJAYggfV1RfSfoQkPqYHp9MwE4IqeYCw9%2BgISDBEZnzV7RRkWRCCCSG3SkuV6IVQoSxKFGFges1glmFKd4GOhswC090EmGIOwmCZ%2FhHEjYA6A6xgpQMAHQxDABIhAwoS%2FY%2FELMnAxTGJawnaIPn5RBT9x%2BYbA%2Fd8oOq%2BwQ%2F3He6Sd5cbme8jlTAFqO90C7oU3VpPoBG2KgyCGKz1FmFgpoawKINQL0yDtKg9eICHuXiCzaYlb2EOXvp0Thdu6PAq4LFxLA%2F8AMB4VEcFIVmAtD%2FSC0MzVBZtOYRBjogRy%2BnL3IgBZY6QFgDvDICbTiEHEsjaGdj8s4cnPWij5mkVT7u0LRPSExnY%2FqFVJwaj8wEXmHZxZrcZUERS%2FECYQwMP5MoQm%2FpSrPDLdgBh7RNSiBDDf7wsDbOqQOJJdagWEQ9JxLV9MIIi%2BxOamkOIO36EKhzKUaoaf1AJzWcyRuhNlDJhqn2Ejzi9JvQRYLALhYnvqEAgb6wXZgZkB%2FOBHGijWyVALpQgskEySgADA7m%2FT3JePIC0SwU0LXAlohoHt6KE0BmIMP83xP%2BW%2BJ%2FyXxCZEetx8R11gHAExXZDekNlwH9msu3aARQH928WAb9I6PM0%2FvXtBo2uVagS9IPIDnPX6XbL9uDp95v6I34hpDegQFnlF0XRKFIBCiQAcWRrwlWTBTc07zURp1YHX2wCHZbCjmYCOjoKA9DgQySAhKZWHGX4qSubqBzz4WEMrcRJYFFazelzqZbDrwTW0AR1DaBFooEQXmWrYeMhzMk1DZEgPfwzpBcUCE8AAuHgVxKEW64uN0Chu8onJAfGZhuyoZLMG7hZMtPFbmEsrxIrkbQZKQFWv4xNOR8zB4hJPSGF4AENHqRC5tKpp2NSu4oB4cJnlCjD1CP6ogwdx2eYnC0tIcosAP1wBrSDXxIdOTAo0hjkvMbCA6R%2BmFBIzC8n9oWEwECUgB7eYmEDwk8I1qIHfyRxFUR%2BS6LNjD7QoNuuQVEaeQqcabSZDGuIY8bAzKDUwRGpANvKBFxOxGn%2FoQAzgQpLBkBAiGMG%2FHREU5TlOE15lFUR07RcwSWJdmApN%2FKFqtmI1pMQmCTUTeEUsnYCVLrFZyAa7QmqOODZAGSNoLgcQCckwm7MRlI6J2MprCsQkz0AvMNBLHCFyNrEiFY7w8iiBzbZDvNw1oYzgELZvtAFjsNpaRRBeyF6o4cL%2FAFBDQYGE%2FOxmM5hKEN4oFDZuH9uFIm8Hk47KHJ42TAMhuoXAsWnv2gaVoGqSH6MGz5BodkYRYcQF4f%2FaAAwDAQACAAMAAAAQerX08iBN1dlc8MHYd1MV5U4MV8MMQ0YuKYw4pY8pserzuZFd9I1AhVc8FbOpodgABto8JTJoF1pBNxaPmlORN4hBBxB88oQ4R15BBB9A88UZEBBBBBh5N88cAgBBBBBJFM888Qo5BBBwI0888884YxgwBs888888gghcd8c88%2F%2FEAB4RAAMAAgMBAQEAAAAAAAAAAAABERAhIDAxQXHB%2F9oACAEDAQE%2FEPAyKe2iit2IXzmcGm7BvTqP%2BCJWkUGNqUYkHBiw1ly3BvJyHplHwNsYmtwhIruPWGiBLc%2BFJqNoHLMJCzPrDYcexU8Lh%2BihYNjYlhqkwwMJIQ%2BDZScIIaRELLTEmLheCF0Xghc2XrUe%2Bw9dFExlwe%2BlejH7x%2F%2FEAB8RAQEBAAICAgMAAAAAAAAAAAEAESExIEEQUTBgYf%2FaAAgBAgEBPxDuwIS2dQQ24ceYOkuZk1huEgbEIMTfNiHuQF0%2FFD%2BtIHywUvPGfqOei5YW1i5wWh97A8wUhLWn3c5vxajkA7tL5puZwhBHLdJ%2FC6gH1IQ%2Bl7%2FV%2FwD%2FxAAoEAEAAgICAQMDBQEBAAAAAAABABEhMUFRYRBxgSAwkaGxwdHw4fH%2F2gAIAQEAAT8QgwqqwZRbZYXYjRqDQqohLhI5lhNiBukNQT4SYLC7YMpDJk0702bw0vaEFLSEo7I3IljPZzg8sECL4EEgVY1CQtpOaTk8zkNx1qxcvQimVpMWkMUZv4hfvzPAMi7BEQ60ZW2XVOu4KaCF88%2BoVDmXFbg5ZyJKo1sRxcSKeoW0pMlTREVgZKC0VGPJzJSma95YqhMGzFrEelKVIr4nwQUyr7kDAA8P6jR5RwEBY3BMXERGQQgsIsUIhtYrEaM5w94hgQVLlQA1XJ6kcEdBQTfxF1xZPBZms5UIKu%2F1xAMghvuh4lXoxGExZUULPyhUVADnuM4LnV%2BbDMm25kFzFBau8L0dwNgD6dMc0Iu1nQN7S6w7EPxF0gQYAAMl43Mx2MX3BXlPKEAuROETYHisQNFauG6SzrE7PW6xEOGf6jiBl7nAJiEp9P7kQ0QC0McStAt19I4fERQdMf2RlWOsKvzCIE1cmHIN22MzBqJoOL9lQuiqN82iyCi1xqGNbphF5c%2FMsHVK1xKgKNaJSmifHyRrNvLBcFkXkKmbfIwLKCgyPZuONYOC2Va44A9au1vwl2A27Ygq0wrnEay7JNoX7qCTDdWUxqytu1Un5hXWQxfuQjp%2F15aVHPKUG15sivda%2FMipmFOYYtJgKYKw5lSWyVdAWjinMG0NUlB8Tj3vj9UoQ53UaSXA3CCPh8y5ylmB9tZ6H4axcVdsNWYxFDzCogshZmtSmpRLFlfjuWBAl5FKUZW1%2Fczdy81m5Vu9Ff1hgYdf%2BEqE8VYDAUmB885J%2Fq947Q5mH%2BTPpNpdkkDK44JMFeu7%2BSRRyXMCnvhInGxxlMywLhfpcWgRKynJnUUe0b1V2p5YDI85IneysIOf1hXSqodA76lNLMcTILfIijcOeIlkUB7kSoF63vFBXzFd1miAcHR9EsWkGpeXLTBk%2FiJJIbhP%2BUQVg1dMrI5s%2BcAtXzUxLFpZ8SMgiwHNkMUsckXXoIrWjzHoZF9AMHMwFMhU01UHlYI%2F2Jl83LwvhIekleiAVXMxAHzchsiBQI3hEjqFrp0NlbfcA2LO%2FNtERxse8plKDfBkf%2Bu5nM7ShbdB6dLm9%2BAoIiKEp1CTyGy6zzCpLAsdDDQxFI%2FPQPxBgCHKxYsgEQPvA6MpV%2BJDZYAOIMsDamj0A6dR7ZF88uUX5gUOLxEJSmU8oZvwgLVCdyouvGZglgXuYaWcu%2BYOY0qGgNTltNJ3GFw%2FekB4XI6qUdRp%2BOYU9y3p03uKbnyN%2FiZzC91AEGLX%2BIrqfe5jUORvmCyt52u%2Fd6XWSA6pJHHlKCoVKFmMLJdP9kBdRuq%2FZUAK3UzDLye8K1s6XEbGzaJmLQdkGmilaUytwUceb7oA4ygANd%2BoltZmXq%2BJa6q4XMi0Qtmob%2BM7S6ylsRtJuKBlLViC%2BYNC7qApUrA3kcX3CvReOPTB3fwXBkizqKIbBeszlMoSthfPwlWzMBDXSZO3yeYzFpCAuaMKlo8dfEI8dueQmyHJAfPKfLfiMPiUq1C4hBYtZYiNHb%2BIA0f8m9VTejbM1YQKoolhdBY3GC5W7uYqB3LWI4E1lfu9HsrjUdbtjJWBtNYuXxCkyr5N0zzUC7iKqEQ2Rg2lZsZf0nx6cuXx602pYVWqodzc28HCDK9wXFrbnn37hLCN3daiby%2BThlW0jWbgbGWTn3YFbYhKhjVOmNA1XH2JdFqGVGpdAwdJjCgfDM4PRsO0GgUaK7jPUGGdN6eo6lc%2BlCyoV1LAYrgioeuD8QBgbt%2B7PP1o2KjH9SBCA3UCivoNy4q%2BZnZ8YLtNQQTiV3KuYNwArYBawsfruWCgHamPwKixBsmhzNBNZpzBsHXoDFphyDV80Td0U41pOeYiBBqmyK0NkKGCiIQo7pBOJVBnXMATiLbf0Y51LSwPmNqDgZyax57%2BkZYtiG9FDFbKKeY56qDWj4G3mYdG90R23v0Xo%2BLmHd8FMhQriG%2B1wl4clu%2FroVqA4ACyVlWigsHy9%2BPpTdNcxCd4ahSiNCjA8n6MxuVotsEwCxz%2BsMHpfBbrMsW%2FjwgEcsjgqKh1gK0V9aUa48wUZjDQFHvccpD0oCRrn6VBIAWbvMovx2bgLD5MszpFImnaWB%2BY7sO6mLL495Y5Gx0%2FbGluuUwxbMwvWtWksm0Murwx8gKIQ5plTxpmACj6b3qrrEVHOCDBQtlS7qPrnLlMlzV0y%2F8AMLQvfNfbritEdBcG4NnVoVLPdQSmwNg7uHODV5%2BlBrxKrxtuIJTqEu3d8E1KVISMbWvlmvP28rNVGIqJmzcNAU5ALyPJENWXWSVX1rQrFLHKuKewOC6QV8mBRX2y6WglqjWwXiE9uQIhA2IJ8%2FZAq9SuSWhiMVIISLFIMnaIuUiq1fC%2BooB92Y1eG%2B%2FrtbgZiLOO0BELch3LnFMKiigTcHY3DA4PspZUQA4Cp0pexiQotAQQS2zVxkzlbj7RgNMIdl%2FWIK2Bel8QpGSGdJa7ldTY6LpRvSaltC5S6uZR5Hj7SjaspxFMPdU2gje%2BuT5lEVx1YXjo%2B7CEA86u4pBb43AqydwCtcSncdq2jEZdo6qaNyiiPDfZHXBvSBOYgjrNRy%2BgIsrBtRZeqtXuK3G%2Be%2FuZAL3GzQq8RSQ0iCaXJLeIyM1JJYIOQb3E1CRgNHR7xdqMMWGBxQQ2Z98yWCBs5UA5W5Th7UKSYBcC%2BLlNv9grmMG2zhOfvc1XbiADwhkmBeO5VyoZFwGF1ZfSjVxcHasFjQ%2FKLhOnwPT5JdXKhdZmwXBTBc2OFEN%2BXLKrLpwezKLKKD6Bojucgx0%2BJQTR119P%2F9k%3D&logoColor=white&logoSize=auto&labelColor=white&color=%23AF001E" style="width: auto; height: 25px;"></a>   <a href="https://github.com/vita-epfl/TIC-TAC"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Code%20(link)-gray?style=flat&logo=GitHub&logoColor=black&logoSize=auto&labelColor=white" style="width: auto; height: 25px;"></a> <a href="https://github.com/vita-epfl/TIC-TAC"><img alt="Presentation" src="https://img.shields.io/badge/Presentation%20(link)%20-%20white?style=flat&logo=googleslides&logoColor=white&logoSize=auto&color=%23C78C06" style="width: auto; height: 25px;"></a><br>

<hr style="border: 1px solid gray;">
<br><br>


## Problem Statement

When heteroscedastic models make predictions, they often estimate:
1. The mean value of the target.
1. The covariance which represents the uncertainty/variability of the target.

However, predicting this covariance is difficult because there are no ground-truth labels for this covariance. The standard approach without the ground-truth covariance relies on optimizing the negative log-likelihood to jointly learn the
mean and covariance. However, recent works show that incorrect covariance estimates can lead to unstable training and ultimately affecting optimization.

![TIC-TAC-pull](https://github.com/vita-epfl/TIC-TAC/blob/main/TIC-TAC_gif.gif?raw=true)
<span style="font-size: 14px; color: darkgray;"> <em>Given samples from a noisy (shown as shaded region) sinusoidal, we compare different methods on their ability to learn the mean and variance.</em></span>

While there have been multiple attempts to address this, we argue that many existing approaches use workarounds and may not truly solve the problem. For instance, recent works proposed different variations of the negative log-likelihood with varying degrees of effectiveness. *Moreover, why should the predicted variance truly represent the randomness of the underlying target?*

Therefore, we propose a solution that directly improves covariance estimation using a more mathematically grounded approach. With the Taylor Induced Covariance (TIC), we tie the predicted covariance to the gradient and curvature of the mean (target) estimator. Intuitively, The gradient and curvature quantify the variation in the prediction within a small neighborhood of the input. Large changes in the target for small changes in the neighborhood of the input should imply larger variance of the prediction.

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/intuition.png?raw=true" alt="TIC-TAC sinusoidal" style="width: 30%; height: auto;">

<br><br>

## Taylor Induced Covariance

With TIC, we propose a new method to parameterise the covariance. Specifically, TIC ties the randomness of the prediction to its gradient and curvature. We do this by representing the input using a stochastic neighbourhood, allowing us to take the second order Taylor polynomial. Specifically, if ε is our stochastic neighborhood, we get
<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/taylor_eq.png?raw=true" alt="Taylor Polynomial" style="width: 40%; height: auto;">
We solve for the covariance of this polynomial through simplifications and some help from our friend, the [Matrix Cookbook](https://www2.imm.dtu.dk/pubdb/edoc/imm3274.pdf). The detailed derivations is provided in Section 3. This gives us the final covariance:
<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/tic.png?raw=true" alt="Taylor Induced Covariance" style="width: 50%; height: auto;">
The presence of the jacobian and hessian allow us to define the covariance using the gradient and curvature of the prediction. We formalize this in the algorithm below.
<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/TIC-algorithm.jpg?raw=true" alt="TIC algorithm" style="width: 50%; height: auto;">
<br><br>

## Task Agnostic Correlations

While we have a new method for covariance estimation, how do we evaluate the covariance? Remember, we do not have labels for the covariance! With TAC, we propose a new metric to directly evaluate the covariance. Specifically, we reason that the goal of estimating the covariance is to encode the relation between the target variables. Therefore, partially observing a set of correlated targets should improve the prediction of the hidden targets since by definition the covariance encodes this correlation. TAC measures this improvement as an accuracy measure for the learnt correlations. We do this by conditioning the predicted target distribution over all but one ground truth, and observe the improvement in the target corresponding to the hidden target variable. If the correlations are learnt correctly, the prediction should update towards the hidden ground truth. By contrast, incorrect correlations move the prediction away from the ground truth. We formalize this through a schematic and algorithm 

*Moreover, TAC and the log-likelihood are complementary: while log-likelihood is a measure of optimisation, TAC is a measure of accuracy of the learnt correlations.*

<div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/tac.png?raw=true" alt="TAC" style="width: 45%; height: auto;">
  <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/tac-algo.png?raw=true" alt="TAC Algo" style="width: 45%; height: auto;">
</div>

<br><br>

## Experiments

We conduct experiments across real and synthetic datasets, spanning univariate and multivariate analysis. Our results show that TIC not only accurately learns the covariance, but also leads to improved convergence of the negative log-likelihood.

<details>
  <summary> <strong>Univariate</strong> </summary>

<img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/univariate.png?raw=true" alt="TIC univariate" style="width: 100%; height: auto;">



We learn constant and varying amplitude sinusoidal with heteroscedastic noise. We observe that TIC accurately learns the variance and improves convergence of the negative log-likelihood. We also observe that modifications to the negative log-likelihood which are not valid distributions may result in unreliable variance estimates. 

</details>

<br><br>

<details>
  <summary> <strong>Multivariate</strong> </summary>

  <div style="display: flex; justify-content: space-between;">
  <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/mv-schema.png?raw=true" alt="TAC" style="width: 45%; height: auto;">
  <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/mv-results.png?raw=true" alt="TAC Algo" style="width: 45%; height: auto;">
    </div> 
 
To evaluate the learnt covariance using ground truth, we setup an experiment with synthetic samples. The schematic is specified above, which allows us to draw samples from heteroscedastic distributions. We compare different methods simulating increasing dimensionality of the data. Our quantitative results show that the gap between TIC and other methods widens.

</details>

<br><br>

<details>
    <summary> <strong>UCI Regression</strong> </summary>

    <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/uci.png?raw=true" alt="TIC univariate" style="width: 199%; height: auto;">

    We conduct experiments on datasets from the UCI Regression repository, and report significant performance gains on most datasets. A curious observation can be made with the Naval dataset, where TIC does not perform as well as other baselines. We note that TIC may not be suitable if all samples have a low degree of variance. A low degree of variance (as indicated by the likelihood) results in accurate mean fits, which implies that small gradients are being backpropagated, and in turn affecting the TIC parameterization. However, we argue that datasets with a small degree of variance may not benefit from heteroscedastic modelling.

</details>

<br><br>

<details>
    <summary> <strong>2D Human Pose Estimation</strong> </summary>

    <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/hpe-qual.png?raw=true" alt="TIC univariate" style="width: 100%; height: auto;">

    We use two architectures: ViTPose and Stacked Hourglass for our studies in human pose estimation. We provide qualitative and quantitative results and show that TIC accurately learns the correlations underlying various human joints. Our qualitative results specifically show that TIC accurately localises the head given the location of other joints. This is especially true for complex poses. Our quantitative results show that TIC scales to both, convolutional and transformer based architectures and outperforms state-of-the-art in learning correlations across various human joints.

    <img src="https://github.com/deep-regression/deep-regression.github.io/blob/master/files/images/tictac/hpe-quant.png?raw=true" alt="TIC univariate" style="width: 100%; height: auto;">


</details>

<br><br>

## Conclusion

Our study is best concluded by the following points:<br>
🔹 Old methods struggle with accurately predicting heteroscedasticity / uncertainty.<br>
🔹 TIC improves this by mathematically modeling how predictions change.<br>
🔹 TAC provides a better way to check if the uncertainty prediction is correct.<br>
🔹 The result? More reliable models that learn faster and make better predictions!<br>


<br><br>

## Acknowledgement

We thank the reviewers, for their valuable comments and insights. We also thank Reyhaneh Hosseininejad for her help in preparing the paper.

This research is funded by the Swiss National Science Foun- dation (SNSF) through the project *Narratives from the Long Tail: Transforming Access to Audiovisual Archives (Grant: CRSII5 198632)*. The project description is available on: [https://www.futurecinema.live/project/](https://www.futurecinema.live/project/)

<br><br>

## Citation

If our work is useful, please consider citing the accompanying paper and starring our code on GitHub!

```
@InProceedings{shukla2024tictac,
  title = {TIC-TAC: A Framework for Improved Covariance Estimation in Deep Heteroscedastic Regression},
  author = {Shukla, Megh and Salzmann, Mathieu and Alahi, Alexandre},
  booktitle = {Proceedings of the 41th International Conference on Machine Learning},
  year = {2024},
  series = {Proceedings of Machine Learning Research},
  month = {21--27 Jul},
  publisher = {PMLR}
}
```
<br>

![TIC-TAC_Poster](https://raw.githubusercontent.com/deep-regression/deep-regression.github.io/master/files/papers/icml/TIC-TAC_Poster.png)

