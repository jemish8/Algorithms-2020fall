# Homework 4

## Read sections 16.1, 16.2, and 16.3 from CLRS
Please read this with the goal of using the knowledge to do the homework below.

## Watch the recorded lectures
- [When is dynamic programming applicable and how to apply it?](https://www.youtube.com/watch?v=G4bsu48KVvs)
- [Example applications of dynamic programming](https://www.youtube.com/watch?v=Y9hfE7Y2hi4)
- [Solving the Matrix-chain multiplication problem using dynamic programming](https://youtu.be/qiB8GmqUJOU)
- [The Alignment Game and the Longest Common Subsequence Problem](https://youtu.be/W-WtMvNdEcM)
- [What is the longest common subsequence problem?](https://youtu.be/k1OmILy0Jmo)
- [Recursive solution for the longest common subsequence problem](https://youtu.be/btmBOSTLyzA)
- [Optimal-substructure property of the longest common subsequence problem](https://youtu.be/gclucr32fHg)
- [Dynamic programming for solving the longest common subsequence problem](https://youtu.be/FG17mqIwGDs)

## Question 1
Explain the 'activity selection problem' by creating a problem of your own. You are free to create any problem, as long as it is similar to a standard activity selection problem.

## Question 2
In Python, implement (a) a recursive solution, (b) a dynamic programming solution, (c) a recursive greey solution, and (d) an iterative greedy solution to the following activity selection problem.

i  |  1 |  2 |  3
-- | -- | -- | --  
si |  1 |  3 |  0
fi |  4 |  5 |  6 

## Question 3 (programming)
For the problem of calculating n<sup>th</sup> Fibonacci number - (a) propose a recursive solution (implementation), (b) a dynamic programming solution using the top-down approach, and (c) a dynamic programming solution using the bottom-up approach. Test the running time of the three implemetations with large values of n and discuss your running time.

## Question 4
What is the matrix chain multiplication problem? Discuss how dynamic programming can be applied to solve it.

## Question 5 (programming)
The "non structural protein 2" (`nsp2`) protein is found to be linked to the mechanism of Coronavirus ([read more](https://onlinelibrary.wiley.com/doi/10.1002/jmv.25719)). Below is the sequence of this protein (first two lines, ignoring the line starting with a hash). In addition to the sequence of this protein, below are the sequences of two other similar (homologous) proteins (see [nsp2.hhba3m.txt](./nsp2.hhba3m.txt) for the alignment). Implement a dynamic programming solution to calculate the longest common subsequence (LCS) between - (a) `nsp2` and `A0A1B3Q5V8` and (b) `nsp2` and `Q9YMB7`. These are two problems that can be solved using the same implementation/code. Lower-case letters in the sequences, if there are any, must be skipped totally. You should print not just the length of the LCS but also the actual LCS.

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

----
# Python implementation of the Huffman's algorithm 
```python
import heapq

def huffman_encode(frequency):
    heap = [[weight, [symbol, '']] for symbol, weight in frequency.items()]
    heapq.heapify(heap)
    while len(heap) > 1:
        lo = heapq.heappop(heap)
        hi = heapq.heappop(heap)
        for pair in lo[1:]:
            pair[1] = '0' + pair[1]
        for pair in hi[1:]:
            pair[1] = '1' + pair[1]
        heapq.heappush(heap, [lo[0] + hi[0]] + lo[1:] + hi[1:])
    return sorted(heapq.heappop(heap)[1:], key=lambda p: (len(p[-1]), p))

data = 'aaccbaaaaaaaaddaaabdebacbaafabaadaaadacabdaefcaaeeaabfdcaaecbbbadafeaaaadadfbdcdabdeccdcadaadbaeaaec'
print('Data:')
print(data)

from collections import defaultdict
frequency = defaultdict(int)

for symbol in data:
    frequency[symbol] += 1

print('')
print('Symbol frequencies:')
print(frequency)

huff = huffman_encode(frequency)

print('')
print('Huffman codes:')
for p in huff:
    print (p[0], str(frequency[p[0]]), p[1])
```
```
Data:
aaccbaaaaaaaaddaaabdebacbaafabaadaaadacabdaefcaaeeaabfdcaaecbbbadafeaaaadadfbdcdabdeccdcadaadbaeaaec

Symbol frequencies:
defaultdict(<class 'int'>, {'a': 45, 'c': 12, 'b': 13, 'd': 16, 'e': 9, 'f': 5})

Huffman codes:
a 45 0
b 13 101
c 12 100
d 16 111
e 9 1101
f 5 1100
```

## Optional Question (not for bonus points)
Discuss how the activity selection problem exhibits the optimal substructure property.

