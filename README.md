ZReviewTender last run status: ![](../../actions/workflows/ZReviewTender.yml/badge.svg)

---
# Deploy ZReviewTender(App Reviews Bot) with Github Action

[![zreviewtender](https://user-images.githubusercontent.com/33706588/184472514-2b8fea8c-c79e-47d9-aa30-ad5376b5823f.jpeg)](https://github.com/ZhgChgLi/ZReviewTender)

Powered by [ZReviewTender](https://github.com/ZhgChgLi/ZReviewTender)

- [\[CH Readme\] ZReviewTender — 免費開源的 App Reviews 監控機器人 - **\[推薦\] 直接使用 Github Repo Template 部署** 區塊 ](https://medium.com/zrealm-ios-dev/zreviewtender-%E5%85%8D%E8%B2%BB%E9%96%8B%E6%BA%90%E7%9A%84-app-reviews-%E7%9B%A3%E6%8E%A7%E6%A9%9F%E5%99%A8%E4%BA%BA-e36e48bb9265)

---

## Pricing

Github Action Proivde `2,000+ mins/month` for free.

ZReviewTender will cost ~= `30s per time`, default run every `6 hours` will cost `4 times/day * 30s/per time * 30days` = `60 mins/month`

I think it's total FREE :)

---

## Setup

### Step 1. Go to [Use this template](https://github.com/ZhgChgLi/ZReviewTender-deploy-with-github-action/generate)
![1_1pn3bxyBO0FoY4oIRvKCNg](https://user-images.githubusercontent.com/33706588/184472590-fc09b717-1184-477c-969d-af2e42606e16.png)

Click [Use this template](https://github.com/ZhgChgLi/ZReviewTender-deploy-with-github-action/generate) on the right-top.

### Step 2. Create Repo
![1_YCBJJlSN4ZYjKMz7WBVIAQ](https://user-images.githubusercontent.com/33706588/184472671-2124e84e-c548-41ed-abf5-2525dd452c0d.png)

- Repository name: type the name you like.
- ⚠️⚠️⚠️ Repo Access: **MUST SET Private**, because you'll upload credentials file (config/private key..) to the repo.

### Step 3. Make sure the repo you've created is Private.
![1_1ZHF9CIOMV8S12Xw2P4B8g](https://user-images.githubusercontent.com/33706588/184472680-4f276b14-c4a6-4302-93a2-b6f9b6f45485.png)

make suer repo you've created have 🔒 icon and Private lable, means it's priave repo.

IF NOT, please change repository visibility to private ASAP.

Repo -> Settings -> General -> Danger Zone -> Change repository visibility -> Make private

### Step 4. wait for Project init success

![](../../actions/workflows/initZReviewTender.yml/badge.svg)

⬆️⬆️ wait for init step success.

![1_jThU3BbKvOT6nl51yklqtg](https://user-images.githubusercontent.com/33706588/184472836-db7f182a-204f-438d-9fcf-a245b8476920.png)

or you can check in Repo -> Actions -> Wait for Init ZReviewTender Workflow -> will get 3 ✅ Init ZReviewTender when execute finished -> Project init Success!

### Step 5. make sure File & Folder has created by Project init step
![1_XEh53SaAjDV9YVk4T41O5Q](https://user-images.githubusercontent.com/33706588/184472920-41371c52-caca-436e-a2d2-fa4164ca30e9.png)

Repo -> Code:
- config/
- config/android.yml
- config/apple.yml
- latestCheckTimestamp/
- latestCheckTimestamp/.keep

make sure your repo has those file & folder above after project init step.

### Step 6. ref [ZReviewTender - Configuration](https://github.com/ZhgChgLi/ZReviewTender#configuration) to fullfill config yml file
- check out [ZReviewTender - Configuration](https://github.com/ZhgChgLi/ZReviewTender#configuration)

![1_SiqBOk6BU38SRJAccC2hEg](https://user-images.githubusercontent.com/33706588/184472980-e1cffa36-3e43-41a9-b86c-462ca0072a0f.png)

- go to config/ folder and full fill android.yml and apple.yml file.
- click ✏️ icon to edit config yml file.

![1_QZ0wQTtbcoN9tgyElYgYAw](https://user-images.githubusercontent.com/33706588/184473018-d375859d-c45d-4998-8972-07ddf384044b.png)

click Commit changes after edited.

![1_pAsWumPT57pLrY3Rn3UZhA](https://user-images.githubusercontent.com/33706588/184473030-12bc512a-d570-4ea7-b722-cd7a95a199ab.png)

![1_CUVQlxKrJjsZZfy3jQErww](https://user-images.githubusercontent.com/33706588/184473059-bdd4190d-f85a-4aee-a97e-44e8039e1b1f.png)

upload releated key file in config/ folder.

### Step 7. init ZReviewTender (manually)
![1_4QTEqr_DeFndqoWuP7YLsQ](https://user-images.githubusercontent.com/33706588/184473096-4558092d-cc47-426e-9bc0-db1144c204fe.png)

Actions -> ZReviewTender -> Run workflow -> Run workflow

![1__zTIiPyGsAejyH1BpggzhQ](https://user-images.githubusercontent.com/33706588/184473129-7ddb2a96-1704-44fc-9c24-b4259cd34d01.png)

- refresh the web, will showing ZReviewTender is running.
- click ZReviewTender go to check running log.
- expend `Run ZreviewTender -r` section to check running log.

![1_SAiaDofDwiFI8Z3ndDGz2w](https://user-images.githubusercontent.com/33706588/184473159-7be52587-ced8-4899-a436-8a05aa90ffbd.png)

if success, no error, you will receive init success message in your slack channel you've specify in config yml.

![1_W5PHoBzHQxV1WQ82TrZqfA](https://user-images.githubusercontent.com/33706588/184473241-caa39ed1-a9eb-4659-b053-c1112e7b872a.png)

### Step 8. Done 🎉 🎉 🎉

ZReviewTender will check latest reviews and resend to your slack channel every 6 hour by deafult.

![183830615-60f5ab30-0e61-4725-be6e-f917fb9589f8](https://user-images.githubusercontent.com/33706588/184503573-40fcce2a-390c-4426-b2b6-7b2a7537eb7a.jpeg)


## Github Action Customize

Actions -> ZReviewTender -> ZReviewTender.yml

![1_DnquiwKTgYY6R2ysNx8F1w](https://user-images.githubusercontent.com/33706588/184473344-03e88bd2-e879-40f6-b04e-f013ab0c51f7.png)
![1_onoSoGPahBOaAsBo6Ou-3g](https://user-images.githubusercontent.com/33706588/184473355-b9e5b3a0-cc3a-4baa-b9d9-698a544b5e90.png)

click ✏️ icon to edit.

![1_HY_f3zOivHGQv5tuwUyw8Q](https://user-images.githubusercontent.com/33706588/184473367-df2cd7db-81b3-44ec-819b-8389b1dc230b.png)

### Edit execute time period

![1_cUGMHPmjlMRV_rRXItN4qg](https://user-images.githubusercontent.com/33706588/184473409-64391df3-3c72-4376-a556-20ac4dd9ffe4.png)

**cron**: execute time period, execute every 6 hour by default `15 */6 * * *`
- you could ref [crontab.guru](https://crontab.guru/) to set time period you wants.
- Github Action timezone is UTC.
- high-frequency will cost more quota of Gihtub Action minutes.

**run**: specify which ZReviewTender command you wnats, uses `ZReviewTedner -r` by default.
- check both android and apple: `ZReviewTedner -r`
- check only apple: `ZReviewTedner -a`
- check only android: `ZReviewTedner -g`
- more command: [ZReviewTender Usage](https://github.com/ZhgChgLi/ZReviewTender#usage)


### Run manually
check step 7.

--

## More Setting/ Report an issue

[ZReviewTender](https://github.com/ZhgChgLi/ZReviewTender)

