# Risk-assessment# EXPERIMENT 4

# ASSET-ORIENTED RISK ASSESSMENT OF STORAGE ASSETS IN AWS

```
NAME   : DANIYEL ANTONY RAJ SD
REG NO : 212224220018
```


## Objective

To identify storage assets in **AWS S3**, identify possible vulnerabilities and threats, and assess their **likelihood, impact, and risk level**.

---

## 1. Software / Cloud Services Required

* AWS Account
* Web Browser
* Internet Connection

### Cloud Services Used

| Cloud Platform  | Storage Service    |
| --------------- | ------------------ |
| AWS             | Amazon S3          |

---

# PART A — AWS S3 STORAGE ASSESSMENT

## Step 1: Login to AWS

1. Open the **AWS Management Console**.
2. Sign in using your AWS account.
3. Search for **S3**.
4. Select **Amazon S3**.

---

## Step 2: Select the S3 Bucket

1. Click **Buckets**.
2. Select the S3 bucket created in the previous experiment.
3. Record:

   * Bucket name
   * AWS Region
   * Number/type of objects

**Screenshot:** S3 Bucket Overview

<img width="1919" height="1004" alt="image" src="https://github.com/user-attachments/assets/8bfdd9f9-b891-464a-83ca-da9f5534db34" />

## Step 3: Check Block Public Access

1. Open the S3 bucket.
2. Select **Permissions**.
3. Locate **Block public access (bucket settings)**.
4. Check **Block all public access**.

### Record

* **ON** → Secure configuration
* **OFF** → Potential public-access risk

**Screenshot:** Block Public Access Settings

<img width="1919" height="993" alt="image" src="https://github.com/user-attachments/assets/126c2fa0-0cad-4ab9-9311-bca9098535bc" />


## Step 4: Check Bucket Versioning

1. Select the **Properties** tab.
2. Locate **Bucket Versioning**.
3. Record whether it is:

   * Enabled
   * Disabled

### Security Purpose

Versioning helps recover previous versions of objects after accidental deletion or modification.

**Screenshot:** Bucket Versioning

<img width="1919" height="1004" alt="image" src="https://github.com/user-attachments/assets/1bb3c6d0-9f00-43d3-8874-69adac3fa8ba" />


## Step 5: Check Default Encryption

1. Stay in the **Properties** tab.
2. Locate **Default encryption**.
3. Record the encryption type.

Possible configurations include:

* SSE-S3
* SSE-KMS
* DSSE-KMS

### Security Purpose

Encryption protects stored data from unauthorized disclosure.

**Screenshot:** Default Encryption

<img width="1919" height="994" alt="image" src="https://github.com/user-attachments/assets/169e8a16-6614-4ed0-8595-15a6c50ee546" />


## Step 6: Check Bucket Policy

1. Select **Permissions**.
2. Locate **Bucket policy**.
3. Check whether a bucket policy exists.

Record:

* Policy exists
* No policy

> **Note:** A missing bucket policy is **not automatically a vulnerability**. Access may be controlled through IAM and other AWS security mechanisms.

**Screenshot:** Bucket Policy Section

<img width="1919" height="990" alt="image" src="https://github.com/user-attachments/assets/ec2917da-adf9-4ac7-8435-03d9d2bd3efb" />

## Step 7: Check Object Ownership and ACL

1. In **Permissions**, locate **Object Ownership**.
2. Record the current configuration.

A common secure configuration is:

**Bucket owner enforced**

This means:

* ACLs are disabled.
* Objects are owned by the bucket owner.
* Access is controlled using policies.

**Screenshot:** Object Ownership

<img width="1919" height="999" alt="image" src="https://github.com/user-attachments/assets/a1b957e0-4e47-4d08-9daa-8519e6d78199" />

## Step 8: Check Server Access Logging

1. Go to **Properties**.
2. Locate **Server access logging**.
3. Record whether it is:

   * Enabled
   * Disabled

### Security Purpose

Logging helps investigate suspicious or unauthorized access to the bucket.

**Screenshot:** Server Access Logging

<img width="1919" height="1023" alt="image" src="https://github.com/user-attachments/assets/95d97a74-4a03-4d38-ac4a-76fc08ddd4f2" />


# PART B — AWS RISK ASSESSMENT

After checking the S3 configuration, identify possible vulnerabilities and threats.

## Risk Formula

**Risk Score = Likelihood × Impact**

### Likelihood Scale

| Score | Description |
| ----: | ----------- |
|     1 | Very Low    |
|     2 | Low         |
|     3 | Medium      |
|     4 | High        |
|     5 | Very High   |

---

## Sample AWS Risk Assessment

> **Important:** Students must use their **actual configuration** while preparing the final table.

| Asset     | Vulnerability            | Threat                                           | Likelihood | Impact | Risk Score | Risk Level | Recommended Mitigation     |
| --------- | ------------------------ | ------------------------------------------------ | ---------: | -----: | ---------: | ---------- | -------------------------- |
| S3 Bucket | Versioning disabled      | Accidental/malicious data deletion               |          3 |      4 |         12 | High       | Enable versioning          |
| S3 Bucket | Access logging disabled  | Difficult investigation of unauthorized activity |          3 |      3 |          9 | Medium     | Enable appropriate logging |
| S3 Bucket | Public access enabled*   | Unauthorized data access                         |          4 |      5 |         20 | Critical   | Enable Block Public Access |
| S3 Bucket | Weak access permissions* | Unauthorized modification/access                 |          3 |      4 |         12 | High       | Apply least privilege      |

---

<img width="2200" height="1250" alt="Screenshot_14_AWS_Risk_Assessment" src="https://github.com/user-attachments/assets/bcc95751-a394-4797-b26c-0d6fae604489" />


# PART C — FINAL RISK SUMMARY

Students should summarize the identified risks.

| Cloud | Asset        | Major Risk          | Risk Level | Mitigation                   |
| ----- | ------------ | ------------------- | ---------- | ---------------------------- |
| AWS   | S3 Bucket    | Versioning disabled | High       | Enable versioning            |
| AWS   | S3 Bucket    | Logging disabled    | Medium     | Enable appropriate logging   |

---
# RESULT

The storage assets in **AWS S3** are identified and analyzed. Various security configurations, vulnerabilities, threats, likelihood, and impacts were evaluated. Risk scores were calculated using the **Likelihood × Impact** method, and appropriate security mitigation measures were recommended.
