# GPT-2 ads

[![Run on Ainize](https://ainize.ai/images/run_on_ainize_button.svg)](https://ainize.web.app/redirect?git_repo=https://github.com/psi1104/gpt2-ads)


GPT-2 model that has been Fine Tuned to generate an advertisement.

- API
    - /gpt2-ads/short: generate words
    - /gpt2-ads/long: generate sentence


- cURL
```bash
curl -X POST "https://main-gpt2-ads-psi1104.endpoint.ainize.ai/gpt2-ads/short" -H "accept: application/json" -H "Content-Type: multipart/form-data" -F "text=My name is Juila" -F "num_samples=5"

curl -X POST "https://main-gpt2-ads-psi1104.endpoint.ainize.ai/gpt2-ads/long" -H "accept: application/json" -H "Content-Type: multipart/form-data" -F "text=My name is Juila." -F "num_samples=5" -F "length=30"
``` 

- Example
    - input : My name is Juila.
    ```bash
        /gpt2-ads/short
  
          {
              "0": " and",
              "1": " T",
              "2": " &",
              "3": " X",
              "4": ","
          }   
    ```
    ```bash
        /gpt2-ads/long
  
          {
              "0": " I love Fashion & Style. Get Your Fashion Styling Dream Job. Enquire Today!\n\nProfessional Stylist Course\nLearn From your Own",
              "1": " I love Fashion & Fashion Styling. Get Your Fashion Styling Dream Job. Enquire Today!\n\nProfessional Styling Course\nStart your career",
              "2": " And I Work for Gmc Sierra.\n\nOnline Interior Design Course\nStart your career Debt Free\nAffordable and flexible payment plans, study at",
              "3": " I love Fashion and Style.\n\nJournalism Courses Online\nWant to write for a living?\nBe A Freelance Journalist.",
              "4": " I love Fashion & Style. Get A Quote Today!\n\nProfessional Styling Course\nHome Study Short Course Online\nGet Your Dream Fashion Styling"
           }   
    ```

