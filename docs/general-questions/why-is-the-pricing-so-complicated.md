# Why is the pricing so complicated?

We are aware of the pricing could be confusing in the beginning - but guess it will make sense when you start using the service.

You will get charged on your monthly subscription date.
The items are:
- **Words** -> The costs for every word (all languages) stored in the version with most words (normally latest)
- **Modifications** -> Any translation (key/value) added, updated or deleted via UI or API (also for empty values)
- **Downloads** -> Every translation file (not word) that gets downloaded from our CDN (if you’re using that feature)
- **Audit entries** -> For every audit entry written if that service is enabled (costs depend on storage duration of the audit logs)

The price per unit go down the higher your numbers are. For details check out the pricing page: [https://locize.com/pricing.html](https://locize.com/pricing.html) (scroll down to the details).


**An example:**</br>
5’000 words * 3 languages -> **15’000 words** * 0.004 -> $60</br>
2000 words changed -> (let’s assume 5 words per key) -> **400 modifications** * 0.04 -> $16</br>
**40000 downloads** * $0.0001 -> $4</br>
$5 base fee</br>
=> Would mean you will be charged around **$85** for you project for that month.</br>
=> For the next month, assuming you don’t change any text (no modifications) and you will not generate any downloads, you will be billed for 20’000 words and the base fee, around **$65**.


We know all those cost units can be confusing - but this is the only way to more or less get a fair pricing for all the different projects out there.
Overall you will see costs below competitors while providing a lot more features.
There is a 14d free trial you can start using without any obligations -> on the billing page you will have an overview over the costs of the current month.

*A little advice: be aware that modifications and downloads are set to zero on subscription.*

</br>

**A simple price calculator:**

[calculator](../calculator.html ':include :type=iframe width=100% height=400px')