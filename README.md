# no-public-s3

What I did:

Wrote a security policy in code
Evaluated real IaC (Terraform) against it
Got a policy-as-code enforcement result

  The Impact
  Imagine pushing this code to production without a policy check. You just exposed your data to the world. With PaC:

  Developers get fast feedback
  Risky misconfigs are caught before they matter
    Compliance teams sleep better

  Mitigate and Retest
  I then made the S3 bucket private.

This policy directly addresses critical security and compliance objectives by satisfying the following NIST SP 800-53 controls:

AC-6(10) – Automated enforcement of least privilege: This policy ensures that permissions for data storage are automatically restricted to the absolute minimum necessary. By preventing public access to storage buckets, it directly enforces the principle of least privilege, reducing the attack surface and mitigating risks associated with over-privileged access. This automated enforcement minimizes the potential for human error in configuring access controls.

SC-12 – Preventing unauthorized public access: The core of this policy is to eliminate the possibility of data being unintentionally exposed to the public internet. By strictly prohibiting public buckets, it acts as a preventative measure against unauthorized disclosure of sensitive information. This control is vital for maintaining data confidentiality and integrity, protecting against data breaches, and ensuring compliance with privacy regulations.
