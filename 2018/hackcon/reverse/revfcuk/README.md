# Reversing 120 - revfcuk

Ignore all the annoying stuff
Interesting stuff starts at 0x401a42
Each 4 bytes of input get double-md5 hashed, and each hash has to match the hash
string at 0x49b180[i<<10:(i<<10)+32] for i in 0..19

    01:$dynamic_2$9f9bd93c746d42c056754dd9607a7ff9
    02:$dynamic_2$5b99e41b25e90adc18f7dcdf8dcb7298
    03:$dynamic_2$95ae5f38b5e4ab0d9d11df14f11046cf
    04:$dynamic_2$f0f7af88ab3aea458526510b1877ab62
    05:$dynamic_2$676d5fb511b9b670b7c9b12c69771f6d
    06:$dynamic_2$6b78f09b932f0519cc29508017bf361d
    07:$dynamic_2$ece3a0446786d5f863ca976fd3c8e2ac
    08:$dynamic_2$e19eca4206a23070180a3a2ec947b3b7
    09:$dynamic_2$b507848b93b4644d0dbf1fc83e8b349c
    10:$dynamic_2$2cac4d5aa5fc42f9d7dfc112bd7fac32
    11:$dynamic_2$55049938be97380188ee360b22a29756
    12:$dynamic_2$cefa5bd3165bb00274063e75bc28014f
    13:$dynamic_2$040a35411852126d8e76c106d867cf8b
    14:$dynamic_2$f99cc38ac9fcae359a14fb5777c42400
    15:$dynamic_2$c4351fcc350e725e7f89b4c2524dd0a9
    16:$dynamic_2$e4f6c86600cae1f5c138ce50d66578dc
    17:$dynamic_2$010a2cbcd80f9f15d421b000f40495b3
    18:$dynamic_2$3e4c9ecd6a2dbbe65369c57a04481431
    19:$dynamic_2$2adc099e0c6bb1d43a08a6c41b2c7220

`john '--mask=?1?1?1?1' '-1=?a?u' hashes.txt`
`d4rk{pr0_at_r3v3rse_4nd_als0_gGWp_Y0u!_4r3_qul7e_gud_@t_thls_pls___teach_me}`