**Which is the default inspection mode on a firewall policy?**

- ~~Proxy based~~
- Flow based

FortiOS supports flow-based and proxy-based inspection in firewall policies. You can select the inspection mode when configuring a policy.

Flow-based inspection takes a snapshot of content packets and uses pattern matching to identify security threats in the content.

Proxy-based inspection reconstructs content that passes through the FortiGate and inspects the content for security threats.

Certain security profiles allows users to display flow-based or proxy-based feature sets.

This following topics provide information about inspection modes for various security profile features:

- Flow mode inspection (default mode)
- Proxy mode inspection
- Inspection mode feature comparison

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/721410/inspection-modes

**How does NGFW policy-based mode differ from profile-based mode?**

- ~~Policy-based flow inspection supports web profile overrides.~~
- Policy-based flow inspection defines URL filters directly in the firewall policy.

Profile-based next-generation firewall (NGFW) mode is the traditional mode where you create a profile (antivirus, web filter, and so on) and then apply the profile to a policy.

In policy-based NGFW mode, you allow applications and URL categories to be used directly in security policies, without requiring web filter or application control profiles.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/978598/profile-based-ngfw-vs-policy-based-ngfw

**Which statement about proxy-based web filtering is true?**

- It requires more resources than flow-based
- ~~It transparently analyzes the TCP flow of the traffic~~

When a firewall policy’s inspection mode is set to proxy, traffic flowing through the policy will be buffered by the FortiGate for inspection. This means that the packets for a file, email message, or web page will be held by the FortiGate until the entire payload is inspected for violations (virus, spam, or malicious web links). After FortiOS finishes the inspection, the payload is either released to the destination (if the traffic is clean) or dropped and replaced with a replacement message (if the traffic contains violations).

To optimize inspection, the policy can be configured to block or ignore files or messages that exceed a certain size. To prevent the receiving end user from timing out, you can apply client comforting. This allows small portions of the payload to be sent while it is undergoing inspection.

Proxy mode provides the most thorough inspection of the traffic; however, its thoroughness sacrifices performance, making its throughput slower than that of a flow mode policy. Under normal traffic circumstances, the throughput difference between a proxy-based and flow-based policy is not significant.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/969330/proxy-mode-inspection

**Which is a valid action for FortiGuard web category filtering?**

- Allow
- ~~Deny~~

| FortiGuard web filter action | Description |
| --- | --- |
| Allow | Permit access to the sites in the category. |
| Monitor | Permit and log access to sites in the category. User quotas can be enabled for this option (see Usage quota). |
| Block | Prevent access to the sites in the category. Users trying to access a blocked site see a replacement message indicating the site is blocked. |
| Warning | Display a message to the user allowing them to continue if they choose. |
| Authenticate | Require the user to authenticate with the FortiGate before allowing access to the category or category group. |
| Disable | Remove the category from the from the web filter profile. This option is only available for local or remote categories from the right-click menu. |

**Which is a valid action for static URL filtering?**

- Exempt
- ~~Warning~~

| URL filter action | Description |
| --- | --- |
| Exempt | The traffic is allowed to bypass the remaining FortiGuard web filters, web content filters, web script filters, antivirus scanning, and DLP proxy operations. |
| Block | The FortiGate denies or blocks attempts to access any URL that matches the URL pattern. A replacement message is displayed. |
| Allow | The traffic is passed to the remaining FortiGuard web filters, web content filters, web script filters, antivirus proxy operations, and DLP proxy operations. If the URL does not appear in the URL list, the traffic is permitted. |
| Monitor | The traffic is processed the same way as the Allow action. For the Monitor action, a log message is generated each time a matching traffic pattern is established. |

**Which action can be used with the FortiGuard quota feature?**

- Monitor
- ~~Shape~~

Quotas can be set for the Monitor, Warning, or Authenticate actions. Once the quota is reached, the traffic is blocked and the replacement message page displays.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/801136/usage-quota

**Which statement about web profile overrides is true?**

- ~~It is used to change the website category.~~
- Configured users can activate this setting through an override link on the FortiGuard block page.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/408599/web-profile-override

**Which is required to configure YouTube video filtering?**

- YouTube API key
- ~~Username~~

If the FortiGuard rating fails, it uses the videofilter.youtube-key to communicate with the Google API server to get its category and channel ID. This is the API query setting and it requires the user’s own YouTube API key string. This configuration is optional.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/860867/filtering-based-on-fortiguard-categories

**Which action can be used with the video FortiGuard categories?**

- ~~Authenticate~~
- Monitor

**Which statement about blocking the known botnet command and control domains is true?**

- DNS lookups are checked against the botnet command and control database.
- ~~The botnet command and control domains can be enabled on the web filter profile.~~

FortiGuard Service continually updates the botnet C&C domain list. The botnet C&C domain blocking feature can block the botnet website access at the DNS name resolving stage. This provides additional protection for your network.

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/105208/botnet-c-c-domain-blocking

**Which security profile inspects only the fully qualified domain name?**

- ~~Web Filter~~
- DNS Filter

**You have configured your security profiles, but they are not performing web or DNS inspection. Why?**

- ~~The certificate is not installed correctly.~~
- The profile is not associated with the correct firewall policy.






NGFW Mode
|-Profile-based
 |-Inspection Mode
  |-Flow-based
  |-Proxy-based
|-Policy-based
 |-Inspection Mode
  |-Flow-based



Web filters are applied in the following order:

1. URL filter
2. FortiGuard Web Filtering
3. Web content filter
4. Web script filter
5. Antivirus scanning

https://docs.fortinet.com/document/fortigate/7.0.5/administration-guide/833698/web-filter



URL filter

------------------------------------------------------------------------------------------
|URL filter type             |Description                                                |
------------------------------------------------------------------------------------------
|Simple                      |The FortiGate tries to strictly match the full context.    |
|                            |For example, if you enter www.facebook.com in the URL      |
|                            |field, it only matches traffic with www.facebook.com. It   |
|                            |won't match facebook.com or message.facebook.com.          |
|                            |When the FortiGate finds a match, it performs the selected |
|                            |URL action.                                                |
|----------------------------|-----------------------------------------------------------|
|Regular expression/ wildcard|The FortiGate tries to match the pattern based on the      |
|                            |rules of regular expressions or wildcards. For example, if |
|                            |you enter *fa* in the URL field, it matches all the        |
|                            |content that has fa such as www.facebook.com,              |
|                            |message.facebook.com, fast.com, and so on.                 |
|                            |When the FortiGate finds a match, it performs the selected |
|                            |URL action.                                                |
------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------
|URL filter action|Description                                                           |
-----------------------------------------------------------------------------------------|
|Exempt           |The traffic is allowed to bypass the remaining FortiGuard web filters |
|                 |, web content filters, web script filters, antivirus scanning, and    |
|                 |DLP proxy operations.                                                 |
|-----------------|----------------------------------------------------------------------|
|Block            |The FortiGate denies or blocks attempts to access any URL that        |
|                 |matches the URL pattern. A replacement message is displayed.          |
|-----------------|----------------------------------------------------------------------|
|Allow            |The traffic is passed to the remaining FortiGuard web filters, web    |
|                 |content filters, web script filters, antivirus proxy operations, and  |
|                 |DLP proxy operations. If the URL does not appear in the URL list, the |
|                 |traffic is permitted.                                                 |
|-----------------|----------------------------------------------------------------------|
|Monitor          |The traffic is processed the same way as the Allow action. For the    |
|                 |Monitor action, a log message is generated each time a matching       |
|                 |traffic pattern is established.                                       |
------------------------------------------------------------------------------------------

Security Profiles > Web Filter > Static URL Filter

-------------------------------------------------------------
|Proxy-Based(Profile)|Flow-Based(Profile)|Flow-Based(Policy)|
-------------------------------------------------------------
|Allow               |Allow              |Allow             |
|Block               |Block              |Block             |
|Monitor             |Monitor            |Monitor           |
|Exempt              |Exempt             |Exempt            |
-------------------------------------------------------------


FortiGuard Web Filtering

------------------------------------------------------------------------------------------
|FortiGuard web filter action|Description                                                |
------------------------------------------------------------------------------------------
|Allow                       |Permit access to the sites in the category.                |
|----------------------------|-----------------------------------------------------------|
|Monitor                     |Permit and log access to sites in the category. User quotas|
|                            |can be enabled for this option (see Usage quota).          |
|----------------------------|-----------------------------------------------------------|
|Block                       |Prevent access to the sites in the category. Users trying  |
|                            |to access a blocked site see a replacement message         |
|                            |indicating the site is blocked.                            |
|----------------------------|-----------------------------------------------------------|
|Warning                     |Display a message to the user allowing them to continue if |
|                            |they choose.                                               |
|----------------------------|-----------------------------------------------------------|
|Authenticate                |Require the user to authenticate with the FortiGate before |
|                            |allowing access to the category or category group.         |
|----------------------------|-----------------------------------------------------------|
|Disable                     |Remove the category from the from the web filter profile.  |
|                            |This option is only available for local or remote          |
|                            |categories from the right-click menu.                      |
------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------
|FortiGuard web filter category|Where to find more information                           |
------------------------------------------------------------------------------------------
|All URL categories            |See Web Filter Categories.                               |
|------------------------------|---------------------------------------------------------|
|Local categories              |See Web rating override.                                 |
|------------------------------|---------------------------------------------------------|
|Remote category               |See Threat feeds.                                        |
------------------------------------------------------------------------------------------

Security Profiles > Web Filter > FortiGuard Category Based Filter

-------------------------------------------------------------
|Proxy-Based(Profile)|Flow-Based(Profile)|Flow-Based(Policy)|
-------------------------------------------------------------
|Allow               |Allow              |Accept            |
|--------------------|-------------------|------------------|
|Block               |Block              |Deny              |
|--------------------|-------------------|------------------|
|Monitor             |Monitor            |                  |
|--------------------|-------------------|------------------|
|Warning             |Warning            |                  |
|--------------------|-------------------|------------------|
|Authenticate        |Authenticate       |                  |
-------------------------------------------------------------


Web content filter

------------------------------------------------------------------------------------------
|Web content pattern type|Description                                                    |
------------------------------------------------------------------------------------------
|Wildcard                |Use this setting to block or exempt one word or text strings of|
|                        |up to 80 characters. You can also use wildcard symbols such as |
|                        |? or * to represent one or more characters. For example, a     |
|                        |wildcard expression forti*.com matches fortinet.com and        |
|                        |fortiguard.com. The * represents any character appearing any   |
|                        |number of times.                                               |
|------------------------|---------------------------------------------------------------|
|Regular expression      |Use this setting to block or exempt patterns of regular        |
|                        |expressions that use some of the same symbols as wildcard      |
|                        |expressions, but for different purposes. In regular expressions|
|                        |, * represents the character before the symbol. For example,   |
|                        |forti*.com matches fortiii.com but not fortinet.com or         |
|                        |fortiice.com. In this case, the symbol * represents i appearing|
|                        |any number of times.                                           |
------------------------------------------------------------------------------------------

Security Profiles > Web Filter > Content Filter

-------------------------------------------------------------
|Proxy-Based(Profile)|Flow-Based(Profile)|Flow-Based(Policy)|
-------------------------------------------------------------
|Exempt              |-                  |-                 |
|--------------------|-------------------|------------------|
|Block               |-                  |-                 |
-------------------------------------------------------------
