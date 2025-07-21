# Security+ Notes - Core Concepts (C.I.A, A.A.A, Zero Trust, Encryption) 

## Key Terms & Concepts

⁃ **CIA TRIAD**
- *Confidentiality*: Prevents unauthorized access
- *Integrity*: Ensures datat isn't altered
- *Availability*: Ensures access when needed

⁃ **AAA MODEL**
- *Authentication*: Verifying user identity
- *Authorization*: Granting access to resources
- *Accounting*: Logging and tracking user activities

⁃ **ZERO TRUST ARCHITECTURE** 

*A security model that eliminates implicit trust and enforces continuous verification and strict access controls.* 

⁃ **PUBLIC KEY INFRASTRUCTURE (PKI)**

*Manages public/private keys and difital certificates for secure communication.*

⁃**STEGANOGRAPHY**

*Hides data inside other media (e.g., images, audio) to avoid detection.*

## Categories of Security Controls
| Category    | Description                                       |
|-------------|---------------------------------------------------|
| Technical   | Tech-based controls (e.g., firewalls, encryption) |
| Managerial  | Policies and procedures for governance            |
| Operational | Day-to-day practices (e.g., incident response)    |
| Physical    | Physical protection (e.g., locks, cameras)        |

## Types of Security Controls

| Type         | Description                                           |
|--------------|-------------------------------------------------------|
| Preventive   | Stop incidents before they occur                      |
| Detective    | Identify and detect incidents                         |
| Corrective   | Mitigate the impact of incidents                      |
| Deterrent    | Discourage attacks or violations                      |
| Compensating | Backup controls when primary ones aren't feasible     |
| Directive    | Provide guidance or instructions                      |

## Zero Trust Control Plane Components

- **Adaptive Identity**: Verifies identity continuously based on context  
- **Threat Scope Reduction**: Minimizes attack surface  
- **Policy-Driven Access**: Enforces access based on defined rules  
- **Policy Engine & Administrator**: Manages/enforces policies


## Encryption Concepts

| Concept               | Description                                               |
|------------------------|-----------------------------------------------------------|
| Symmetric Encryption   | One key for encryption and decryption                     |
| Asymmetric Encryption  | Uses a public/private key pair                            |
| Encryption Layers      | Disk, file, volume, database, transport-level encryption  |



## Must-Know Facts

- **CIA Triad**: Confidentiality, Integrity, Availability  
- **AAA**: Authentication, Authorization, Accounting  
- **Security Controls**: Preventive, Detective, Corrective, etc.  
- **PKI**: Manages keys and digital certificates  
- **Symmetric vs. Asymmetric**:  
  - Symmetric = 1 key  
  - Asymmetric = Public + Private keys



## Reference Concepts

- **Zero Trust Architecture**: Continuous verification  
- **Change Management**: Mitigates risks from system changes  
- **Digital Signatures**: Authenticate sender + ensure data integrity  
- **TPM (Trusted Platform Module)**: Secure hardware for cryptographic keys



## Concept Comparisons

| Concept              | Description                                      | Key Differences                         |
|----------------------|--------------------------------------------------|------------------------------------------|
| Honeypot             | Single decoy system                              | One system vs. a whole network (honeynet) |
| Honeynet             | Network of decoy systems                         | A network of systems vs. a single system                                         |
| Symmetric Encryption | One key for both encryption and decryption       | One key vs. two keys in asymmetric       |
| Asymmetric Encryption| Public key for encryption, private key for decryption | Two keys vs. one key in symmetric     |
