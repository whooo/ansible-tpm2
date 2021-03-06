# ansible-tpm2
Ansible role for TPM 2.0 tasks

PoC for working with TPM 2.0 using ansible.
The following functions are currently supported:
* Generate an EK and get the certificate
* Verify the EK against certificate and the certificate against a CA
* Create an AK
* Handle the MakeCredential and ActivateCredential procedure
* Get a quote and verify it using the AK
* Get the UEFI event log and verify it against the quote

See example.yaml

Requires tpm2-pytss >= 0.1.8 locally and on the remote host as well as pyca and the openssl cli tool locally.

# TODO
* Move usual functions out of plugins/modules into module_utils
* Create supporting functions/class for all modules
* tpm2_quote should take a TPMS_PCR_SELECTION as argument instead of a digest algorithm name
