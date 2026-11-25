
# Experiment 4 – Asset-Oriented Risk Assessment of Storage Assets in AWS

# Name  : SANTHOSH KUMAR V
# Reg No: 212225040381

## Objective
To identify storage assets in AWS S3, examine their security configurations, identify possible vulnerabilities and threats, and assess their likelihood, impact, and risk level.

## Software / Cloud Services Required
- AWS Account
- Web Browser
- Internet Connection
- Amazon S3

## Cloud Service Used

| Cloud Platform | Storage Service |
|---|---|
| AWS | Amazon S3 |

---

## PART A – AWS S3 STORAGE ASSESSMENT

### Step 1: Login to AWS
1. Open the AWS Management Console.
2. Sign in using your AWS account.
3. Search for S3.
4. Select Amazon S3.

### Step 2: Create an S3 Bucket
1. Navigate to Amazon S3 → Buckets.
2. Select Create bucket.
3. Enter a unique bucket name.
4. Select the required namespace.
5. Configure the bucket settings.
6. Review the configuration.

**Bucket Creation Details:**

| Parameter | Observation |
|---|---|
| Bucket Name | exp5-jayanin |
| Namespace | Global namespace |
| Object Ownership | Bucket owner enforced |
| ACLs | Disabled |

**Screenshot 1 – S3 Bucket Creation Configuration**

<img width="1881" height="772" alt="Screenshot 2026-11-21 224334" src="https://github.com/user-attachments/assets/83b5bff2-c0b6-4236-b60a-29fad673f579" />


### Step 3: Configure Object Ownership
1. Locate the Object Ownership section during bucket creation.
2. Select ACLs disabled (recommended).
3. Verify that Bucket owner enforced is displayed.

**Security Observation:**
- ACLs are disabled.
- All objects are owned by the bucket owner.
- Access to the bucket and its objects is controlled using policies.

<img width="1906" height="767" alt="Screenshot 2026-11-21 224341" src="https://github.com/user-attachments/assets/9940bda5-1b5b-4a05-9e7a-a23cfed71aff" />
<img width="1875" height="433" alt="Screenshot 2026-11-21 224348" src="https://github.com/user-attachments/assets/41af1c81-c387-4698-a587-7555ebde9abf" />
<img width="1892" height="447" alt="Screenshot 2026-11-21 224354" src="https://github.com/user-attachments/assets/cff30544-da4b-47f3-a9af-43ef4ab5a2d0" />


### Step 4: Upload Objects to S3
1. Open the S3 bucket.
2. Select Upload.
3. Add the required files.
4. Select Upload.
5. Verify the upload status.

**Upload Observations:**

| Parameter | Observation |
|---|---|
| Destination Bucket | exp2-bucket-jayani |
| Files Uploaded | 3 |
| Total Size | 2.5 MB |
| Successful Uploads | 3 |
| Failed Uploads | 0 |
| Upload Status | Succeeded |

**Screenshot 2 – Successful File Upload**

<img width="1070" height="457" alt="Screenshot 2026-11-21 224505" src="https://github.com/user-attachments/assets/b2828668-cd54-4390-917f-81b827f4ec58" />


---

## PART B – AWS RISK ASSESSMENT

### Risk Assessment Method

Risk Score = Likelihood × Impact

**Likelihood Scale**

| Score | Description |
|---|---|
| 1 | Very Low |
| 2 | Low |
| 3 | Medium |
| 4 | High |
| 5 | Very High |

**Impact Scale**

| Score | Description |
|---|---|
| 1 | Very Low |
| 2 | Low |
| 3 | Medium |
| 4 | High |
| 5 | Very High |

### Observed Security Configuration

| Security Control | Observation | Security Significance |
|---|---|---|
| Object Ownership | Bucket owner enforced | Objects are owned by the bucket owner |
| ACL Configuration | Disabled | Prevents ACL-based access management |
| File Upload | Successful | 3 files uploaded successfully |
| Upload Failures | 0 | No upload failures recorded |

### Potential Risk Assessment

The following table identifies potential risks to evaluate. These are assessment scenarios, not confirmed vulnerabilities in the observed bucket.

| Asset | Potential Vulnerability | Threat | Likelihood | Impact | Risk Score | Risk Level | Recommended Mitigation |
|---|---|---|---|---|---|---|---|
| S3 Bucket | Public access enabled | Unauthorized data access | 4 | 5 | 20 | Critical | Enable Block Public Access |
| S3 Bucket | Versioning disabled | Permanent data loss | 3 | 4 | 12 | High | Enable bucket versioning |
| S3 Bucket | Access logging disabled | Difficult security investigation | 3 | 3 | 9 | Medium | Enable appropriate logging |
| S3 Bucket | Excessive permissions | Unauthorized access or modification | 3 | 4 | 12 | High | Apply least privilege |

---

## PART C – SECURITY RECOMMENDATIONS

1. Enable Block Public Access to prevent unintended public exposure.
2. Enable S3 Versioning to recover accidentally deleted or modified objects.
3. Enable appropriate logging to monitor bucket activity.
4. Apply least-privilege IAM permissions.
5. Use server-side encryption to protect stored data.
6. Regularly review bucket policies and access permissions.
7. Disable ACLs and use policy-based access control where appropriate.

---

## PART D – FINAL RISK SUMMARY

| Cloud | Asset | Potential Risk | Recommended Mitigation |
|---|---|---|---|
| AWS | S3 Bucket | Public data exposure | Enable Block Public Access |
| AWS | S3 Bucket | Accidental data deletion | Enable Versioning |
| AWS | S3 Bucket | Insufficient activity monitoring | Enable Logging |
| AWS | S3 Bucket | Excessive permissions | Apply Least Privilege |

---

## PART E – AZURE BLOB STORAGE

Azure Blob Storage assessment was not performed because an Azure account was not available for this experiment.

Therefore, the assessment was limited to Amazon S3.

---

## PART F – SCREENSHOTS

### AWS S3
1. S3 Bucket Creation Configuration
2. Successful File Upload

---

## RESULT

The AWS S3 storage asset was examined, and its object ownership and ACL configuration were identified. Three files with a total size of 2.5 MB were successfully uploaded, with no upload failures.

Potential storage security risks, including public access, disabled versioning, insufficient logging, and excessive permissions, were identified along with appropriate mitigation measures.

The experiment demonstrated the importance of asset-oriented risk assessment and secure storage configuration in AWS.
