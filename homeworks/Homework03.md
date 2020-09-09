# Homework 3

# Read sections 15.2, 15.3, and 15.4 from CLRS
Please read this with the goal of using the knowledge to do the homework below.

# Watch the recorded lectures
- [When is dynamic programming applicable and how to apply it?](https://www.youtube.com/watch?v=G4bsu48KVvs)
- [Example applications of dynamic programming](https://www.youtube.com/watch?v=Y9hfE7Y2hi4)
- [Solving the Matrix-chain multiplication problem using dynamic programming](https://www.youtube.com/watch?v=xCzt0mRN10c)
- (ToDo)
- (ToDo)

# Question 1
Discuss a problem where dynamic programming is not applicable and explain why dynamic programming is not applicable to the problem.

# Question 2
With the help of an example, discuss the steps involved in developing a dynamic programming algorithm to solve a problem.

# Question 3 (programming)
For the problem of calculating n<sup>th</sup> Fibonacci number - (a) propose a recursive solution (implementation), (b) a dynamic programming solution using the top-down approach, and (c) a dynamic programming solution using the bottom-up approach. Test the running time of the three implemetations with large values of n and discuss your running time.

# Question 4
What is the matrix chain multiplication problem? Discuss how dynamic programming can be applied to solve it.

# Question 5 (programming)
The "non structural protein 2" (`nsp2`) protein is found to be linked to the mechanism of Coronavirus ([read more](https://onlinelibrary.wiley.com/doi/10.1002/jmv.25719)). Below is the sequence of this protein (first two lines, ignoring the line starting with a hash). In addition to the sequence of this protein, below are the sequences of two other similar (homologous) proteins (see [nsp2.hhba3m.txt](./nsp2.hhba3m.txt) for the alignment). Implement a dynamic programming solution to calculate the longest common subsequence (LCS) between - (a) `nsp2` and `A0A1B3Q5V8` and (b) `nsp2` and `A0A1B3Q5V8`. These are two problems that can be solved using the same implementation/code. Lower-case letters in the sequences, if there are any, must be skipped totally.

```
# The lines starting with > are header lines that are the names of the sequence
# Lower-case letters in the sequences must be skipped totally.
>nsp2
AYTRYVDNNFCGPDGYPLECIKDLLARAGKASCTLSEQLDFIDTKRGVYCCREHEHEIAWYTERSEKSYELQTPFEIKLAKKFDTFNGECPNFVFPLNSIIKTIQPRVEKKKLDGFMGRIRSVYPVASPNECNQMCLSTLMKCDHCGETSWQTGDFVKATCEFCGTENLTKEGATTCGYLPQNAVVKIYCPACHNSEVGPEHSLAEYHNESGLKTILRKGGRTIAFGGCVFSYVGCHNKCAYWVPRASANIGCNHTGVVGEGSEGLNDNLLEILQKEKVNINIVGDFKLNEEIAIILASFSASTSAFVETVKGLDYKAFKQIVESCGNFKVTKGKAKKGAWNIGEQKSILSPLYAFASEAARVVRSIFSRTLETAQNSVRVLQKAAITILDGISQYSLRLIDAMMFTSDLATNNLVVMAYITGGVVQLTSQWLTNIFGTVYEKLKPVLDWLEEKFKEGVEFLRDGWEIVKFISTCACEIVGGQIVTCAKEIKESVQTFFKLVNKFLALCADSIIIGGAKLKALNLGETFVTHSKGLYRKCVKSREETGLLMPLKAPKEIIFLEGETLPTEVLTEEVVLKTGDLQPLEQPTSEAVEAPLVGTPVCINGLMLLEIKDTEKYCALAPNMMVTNNTFTLKGG
>A0A1B3Q5V8
FLTDQYGFDADGVLAAPIKEVLGDKGAGMSlveltkflgkyRTADGYELPSGIVKVAVKVVRKNLPVSKQSIFTVLGVTERVVDGFYYPYSTNSVVSYTKPRAGATVGNTVQSVMLSVYGTEAYNPVTPVVRLRCSSCDFYGWVPVKDLGCVTCSCAAVHQitsSCIDAESAGLIKQGAVMLVDRSPSMRVVPGNRlYVAFGGAIWSPIGKVNGVQVWVPRAYSCVAGDHSGAVGSGDVnTINKEIMSLIIDGVRIDDEVLEQPSCGVLIANLEDPSAAPRVHTVDSLRQLCVDNNvmlgDTplpKDEFHPgivGLSYHFYRACWYGVLTAKSFGAFKELLQSEEVRLSHFCANIRRCLDRALNWARTTGnvsllssSLVLKALAENLLDSVKNTPFLVGDLVKPVLDWIVEKMVLARDSVVSCAEAVLSLFNMQFTFAKGKFTFLKEKLNKSCVALRELLTVIVNKFATTVKWAGCKIDGFYNGDYHFFSAKGVLTEVQVCAKTLGAMLtPRQQRMEVEVLDGKYdAPVAITVPELEELNGTLEEVFGFDDLTLVRGSLVALASKVFVRTDDGLLFRYVKSGGVFLKAFRLRGG
>Q9YMB7
YVDQYMCGADGKPVieGDFKDYFGDEDIIEFEGEEYHCAWTTVRDEKPLNQQTLFTIQEIQYNLDIPHKLPNCATRHVAPPVKKNSKIVLsedYKKLYDIFGSPFMGNGDCLSKCFDTLHFIAATlRCPCGSESSGVGDWTGFKTACCglSGKVKGVTLGDIKPGDAVvtsMSAGKgVKFFANCVLQYAGDVEGVSIWKVIKTFTVDETVCTPGFEGELNDFIKPESKSLVACSVKRAFITGDIDDAVHDCIITGKLDLSTNLFGNVGlLFKKTPWFvQKCGALFVDAWKVVEELCGSLTLTYKQIYEVVASLCTSAFTIVNYkpTFVVPDNRVKDLVDKCVKVLVKAFDVFTQIITIAGIEAKCFVLGAKYLLFNNALVKLVSVKILGKkQKgLECAFfatsLVGATVNVTPKRTETATISLNKVDDVVAPGEGYIVIVGDMAFYKSGEYYFMMSSPNFVLTNNVFK
```

# Question 6 (programming)
Implement a dynamic programming solution to calculate the longest common subsequence (LCS) of `<1,0,0,1,0,1,0,1>` and `<0,1,0,1,1,0,1,1,0>` (CLRS: 15.4-1). 

