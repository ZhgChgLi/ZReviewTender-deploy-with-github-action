# Deploy ZReviewTender(App Reviews Bot) with Github Action

[![183288627-209506d5-1e77-4ab9-b9c2-029e291fc06c](https://user-images.githubusercontent.com/33706588/183292970-46e3dccf-0d32-4bb8-bc5c-5867035bf2d6.jpeg)](https://github.com/ZhgChgLi/ZReviewTender)


Powered by [ZReviewTender](https://github.com/ZhgChgLi/ZReviewTender)

---

## Setup

### Step 1.
![ZhgChgLi_2022-08-07_20-47-56](https://user-images.githubusercontent.com/33706588/183291986-a7a563d1-f6d0-49df-9fd0-cf6313d33917.jpg)

Click [Use this template](https://github.com/ZhgChgLi/ZReviewTender-deploy-with-github-action/generate) on the right-top.

### Step 2.
![ZhgChgLi_2022-08-07_20-49-09](https://user-images.githubusercontent.com/33706588/183292060-e665c166-9389-44e7-85ba-94c8d4c3e684.jpg)

- Repository name: type the name you like.
- ⚠️⚠️⚠️ Repo Access: **MUST SET Private**, because you'll upload credentials file (config/private key..) to the repo.

### Step 3.
![ZhgChgLi_2022-08-07_20-50-51](https://user-images.githubusercontent.com/33706588/183292176-8ec9a3bf-5021-4077-a1f5-562649dac642.jpg)

go to /config after repo created.

### Step 4.

![ZhgChgLi_2022-08-07_20-51-13](https://user-images.githubusercontent.com/33706588/183292226-baad75e3-6e41-48c0-9cce-915fef46e49e.jpg)

edit android & apple config yaml file.

![ZhgChgLi_2022-08-07_20-51-25](https://user-images.githubusercontent.com/33706588/183292253-bb6446f5-d563-427a-9670-e6b32327feef.jpg)

![ZhgChgLi_2022-08-07_20-52-49](https://user-images.githubusercontent.com/33706588/183292261-dda5531d-2026-4ec2-8cc2-3ade968e3a9f.jpg)

* rememver rename the file name to `apple.yml`

![ZhgChgLi_2022-08-07_20-54-03](https://user-images.githubusercontent.com/33706588/183292265-8f6037bf-c3bc-4aa3-8a57-bb43fba0343f.jpg)

same as apple.yml

* rememver rename the file name to `apple.yml`

### Step 5. upload dependency credentials


![ZhgChgLi_2022-08-07_20-54-24](https://user-images.githubusercontent.com/33706588/183292354-36865474-a4d7-4377-8040-a8ba6d5a11ba.jpg)

![ZhgChgLi_2022-08-07_20-54-59](https://user-images.githubusercontent.com/33706588/183292364-e0c18816-8d7c-4572-b43f-4f265ddc25b1.jpg)

upload the file you specify in apple/android.yml e.g. `AuthKey_XXX.p8`, `android_publisher_key.json`

### Step 6. init ZReviewTender

![ZhgChgLi_2022-08-07_20-55-39](https://user-images.githubusercontent.com/33706588/183292458-838929e8-0449-4c1c-8c4f-513988a4b7b6.jpg)

go to `Actions` -> `ZReviewTender` -> `Run workflow` -> `Run workflow`

![ZhgChgLi_2022-08-07_20-56-24](https://user-images.githubusercontent.com/33706588/183292496-f67de687-6da8-40ff-ad0a-f49f349b7188.jpg)

back to slack channel, you'll receive an init success message in channel!

### Done

![ZhgChgLi_2022-08-07_21-02-30](https://user-images.githubusercontent.com/33706588/183292531-f7caa7bb-7337-4291-86bd-76c60a893c04.jpg)

ZReviewTender will check the latest review every 6 hours, and resend review to slack channel automatically, like above :).

---

## Q&A

### Change the checker schedule

![image](https://user-images.githubusercontent.com/33706588/183292653-a0de62a4-0cad-4684-92af-fb23b1b58c64.png)

![image](https://user-images.githubusercontent.com/33706588/183292673-36b3c50a-d663-4823-9ff5-075dce25a052.png)

![image](https://user-images.githubusercontent.com/33706588/183292704-285cb381-c4cc-4731-9707-9121a6fada60.png)

you can change the crontab setting by modify `cron` parameter. [crontab](https://crontab.guru/)

### Only check App Store or Google Play Review

ZReviewTender will check bot App Store and Google Play review by default.

![image](https://user-images.githubusercontent.com/33706588/183292851-724564e6-7ab3-4a59-a715-2dcfe3653444.png)

you can modify command to:

- Both (Default): `ZReviewTender`
- Only Apple Store(iOS): `ZReviewTender -a`
- Only Google Console(Android): `ZReviewTender -g`

--

## More Information/ Report an issue

[ZReviewTender](https://github.com/ZhgChgLi/ZReviewTender)

