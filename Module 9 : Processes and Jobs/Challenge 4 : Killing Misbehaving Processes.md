# Killing Misbehaving Processes
This challenge requires us to use the 'kill' command to kill a decoy process hogging the named pipe(FIFO).
## My Solve
**Flag:** 'pwn.college{glDkcfo0ULrWybsv-Q2J-UDBs1L.0FNzMDOxwSOxkjNzEzW}'

I first listed all the processes related to decoy and found the PID value for /challenge/decoy (142). On killing the 
process, I run /challenge/run which sent the flag to /tmp/flag_fifo. I used cat to read contents of the fifo which contained
lots of decoy flags. I terminated the process and ran /challenge/run again which sent the flag to the fifo. On reading the 
fifo again, I could see the required flag.
```
hacker@processes~killing-misbehaving-processes:~$ ps aux | grep /challenge/decoy
root         139  0.0  0.0   5204  3520 ?        S    06:05   0:00 su -c exec /challenge/decoy > /tmp/flag_fifo hacker
hacker       142  0.0  0.0  13516  9280 ?        Ss   06:05   0:00 /usr/bin/python /challenge/decoy
hacker       185  0.0  0.0 230696  2560 pts/1    S+   06:06   0:00 grep --color=auto /challenge/decoy
hacker@processes~killing-misbehaving-processes:~$ kill 142
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
^C
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{NmNTXTDasntNjxHu5sYNZTYL43bfJKu9C.sWUHggd6-I32M}
pwn.college{wYxbiq-2PndpDEoJWLAyfFis9fPUM8zc6iqVEhxK.P58rlg}
pwn.college{xnaqXs0FP8j1TO4gytsGOa6qSW2jM9D4CzfVIvsvYBygmx0}
pwn.college{k.R6WSDFbmwg6blE2bSLopS2UJaxO8.2EC0bHL20hHLU-kD}
pwn.college{G9r9OUFwvuSfUoUPhhDaom7-cmWHCr5WISLo5ecEIGqY09A}
pwn.college{xOsFmVRhZ7FczGE9wi7f-PErpJ4vVPAulP3JX9ztexYEr31}
pwn.college{TEj4cd0-R9WVqWQs5E1GY-Q8hxu.cF82nhGiTyQZWDAqDXF}
pwn.college{Y.dx2gEJBdGF1W4QhH6qMTx7QThrxp4fNjn8mUIWyQQuRV.}
pwn.college{0.mHXowVifjbQs3jBl23WsKZng0cAgjMWzw3jgKbsbX3tqr}
pwn.college{w8jy9XPtpMOhfGBWOm8d7avAFzABLj1TWuG16RC7mcO0ZZV}
pwn.college{RSPo07bgqsafDBc0S6thrtO9XNZRzcH7yUkV3BodfSInmzd}
pwn.college{tWm61yp-Lie.4-ThNqDA6dWswL7KYAF0wDQG-8nH5x10QSd}
pwn.college{1bd9RbT7ahD1oY45d1qiErp6O.B7tl2iMpjnhu6mA7GYjAB}
pwn.college{T2sfBHD2yoHYWLTX8Z.vimsTAz7SH8P1.LzUb9aL7w4wP5b}
pwn.college{YNVTpFVenrj1ldYAaq99OmFxxBOqYrtwbLLTTxJ-iSgDl8P}
pwn.college{k9Jkk-ZxMchqkISHZ8dHTzwNn9aq.THL15sJGl.4wg0xc6H}
pwn.college{c4MM.DudSu1-lhPDvTiH6wAXA8eI9USJrgZc6trnEdRSsmI}
pwn.college{fqpZPJ0yqb8iqDv4XFpxwBqs0XE2.8CK0ctBTPxP9kkRvcy}
pwn.college{QOKCZNAEKHTgIRd5hdtH1ZlHUlwGQ0Hrz.Sgy38x2f.F67c}
pwn.college{CpfpGZ17-Q0JCtIDH.UyliKYCGkDUwlJH9cxyReHAy04ZjS}
pwn.college{kEIHDm4sKy6CGY4-6k2pitOubvwDBMLuF.qGGyzeLk94XWI}
pwn.college{PWdQVelPRjrSmrrUhTt1Kr41ATwXeBAh7asDsVcQFH9nwBP}
pwn.college{zcg-pQy6zOqVtPFM6Wtv4sl3Nc7RfFVsGYfKEbjcpE6A1so}
pwn.college{gvmDNAzBP41EaMPlc8euslvHt4yNAuyxl217Oe2JdkiWhRK}
pwn.college{499v-nMpds-ShjuiFL0vMtxXAxKFY8vIX1l9jxweYFcIJto}
pwn.college{beBAqz2BWgg7ax60yr-a8Y80e1MyQhsJ617NA7hDf9ilIMs}
pwn.college{4LEMxv2QECKy81I2FvfqcwQFowM0s4C9B.2usjNHMrsO3Hp}
pwn.college{zAj4sy1gWdrSQ9BnXiUcPTi8jVroRxCszQXpycAIYpkeEA6}
pwn.college{V8hmeGQseHPWQhTtGNjP4EVOncbpnFxGLEfFtIwci9Yfbmp}
pwn.college{A.apk6GenPeKdzUuIipiUG3xC5sIccLf1TrP4F0.cbQnpMm}
pwn.college{ObrtxwyAzKw.9HmFiaXYj6VvpkcurhhRouBRB1lNzlr4CRX}
pwn.college{xdBk0jeoxJcdAOZre3LfyH1vafHKqZqrfgSpsm8Dr2hStQt}
pwn.college{hsfErBpUVRz48vIu3sGaH-YTJm3WArh1ifausUTxSmwJgCN}
pwn.college{0nGVLfmSFzO0EpPRFrCmuEMSpW-IEGYJseKe1t6nAa30-ok}
pwn.college{SKq12EkjL.om8EhVGUTYPM0xAafxkJZ9Ip4UHMVRAIPi5bA}
pwn.college{SXIWV8IIwbxi9pnLLcpR6xDdeRVZywzVCqDwXW6Q5T4QOg0}
pwn.college{Wvf6NSebJ0zLfYo8N5Ij.r0bL0EedoNBeMNJHyPd82Ow8Zn}
pwn.college{IZTwgle20SnszETYFopo.Elt62ol4nFPXxigCvoDCe80ZFn}
pwn.college{YfvS2.731.3SrH3gEnI25t1NNWVCKmZaMbOapnkp1nptU6s}
pwn.college{PoCMeiYPjKazR9RLHscNVyoL3xIPurohFvVkB.QeeMMf3AX}
pwn.college{0Zk4chr.fW86E.pV9sF-5B8nQs2GhEFCHUAjXN5p4jnNxo6}
pwn.college{VPGl2f8r1Hpb9BCQjMl1-uy0WHob8CrwZhoTHOIqkiawR5G}
pwn.college{..7w7KdZXjHIrj36ITT7uLIBgK1P9GOzQgayYYSNQSYtrWo}
pwn.college{nCjJ7inB2VLJvDoIkxkD2pnqUts.2D6efI-Ul3eUu0Xpe3N}
pwn.college{PHPvw2w7iBjxv96OQchwkJBvU0Es9IYf-oTeDq5W5b8tXDS}
pwn.college{XCG.g2qCqTt5EUQUDFLOz4fE7JoL9254yoZChNrzSR.O5fW}
pwn.college{YHw-iaaBFS5Tj2XoZQXoIo1HPuD29pI5LWmpKRteKnyrG.z}
pwn.college{oLwXVQ0nxxgIO-q1SElT87MwRENPMfWO.f.GFhlg215TjXS}
pwn.college{WBEZu616BdYpl1v.lWsB3hqN69R604VJMPyQ0905qpAt-u1}
pwn.college{vVkVaJCTsLJ.RF8JWmZN1joY8foUgeUtpiBFOJyViVw.va2}
pwn.college{cg7lGW3MX.E4mExv393U.vRMnbcy1T4uOx96af72tcE4nG2}
pwn.college{P1FOtCY2MW52L96HcIHElnR8s0iQ.gyaKzYK.aFIg.FZW.S}
pwn.college{06QhDVx2lxdxehU12BhOUVbvhULifU9-CF-AZ1IWrWQXb.I}
pwn.college{HEPSyyuLEg1rQhkJJEKY5heQrZtZ2L0vF5.SMBimFm3poeA}
pwn.college{KOoWDKhpPecNI4ChJshsDYTYbbDiriPc8xDi1OlFiXYOViu}
pwn.college{WpV9.ZtsmLAzfNTNc8mGhpfuPxMv1sIi6rgUHZF30f-CYWL}
pwn.college{4xQBcPrijKhs0uLRY7lu3i-2gUw190M58lNTm2XhgObI4ow}
pwn.college{-in8IbDbNGv0RSzqto5n7jJAD4U.e3EVDf7Rb44r.zYDDDc}
pwn.college{nPBhNY..lMtbfMH1pv0-d67Wloqh1GCnY59WN4AQsB9RaEK}
pwn.college{-OAew2xNHTlgCUrHF4Sn2GP5M3FQtXi8Kka07HN6b58YsZo}
pwn.college{XSU.-a2HCh8aycQj3MPhFatLTiTYFXuwS21gV884DLbul4H}
pwn.college{pXUZ.QZdnntF9UfMDsgZMNv73tE2YyrKoriNqmVUbqHPuDZ}
pwn.college{csgN9iOUUfhmzz6N6JDXHtS9Jmj1789gRfWzUIjdeJh1Lx5}
pwn.college{C4g7AWuMH2ZM-pq9czZIgM5fcPwMGVZtQkI-aV4k6TzCjFC}
pwn.college{NeA2KWyd6Yrn2ASwtC8AoVEccfK05GsFaYwh0.VIANh2EwI}
pwn.college{9melYdkb8.McWnGpIC.7FHhUZVTBuTINXFVm8YOijuO1o1R}
pwn.college{4gkfXFoPQnzR-X4Imvsec01BOTjkPDbOyz.2H5U92NaX2h.}
pwn.college{NBNTsSiL.GlxNoj4pZHzB2UPKKHyzIhcJqHpMLBrdwglfXe}
pwn.college{UAj7QVJdqxvy.247LbdvMScAF0a9jict57pFqoyyIEt1ZhC}
pwn.college{Jo0QIofLrHhUelJdPBdtHdSBEbE70DTvVmRIJaaY94UXRdd}
pwn.college{XuLmXDhFAMwtCNbf7dnxMPXWGJFVYj7eCPButWBNCQOlA2V}
pwn.college{hIXDdT2QDMH16IAUgqXdcIqCoet0pF-4WjgUd5kEHPDFhyr}
pwn.college{F4bvQMB9YtwzvAB4jcqXxZ.TYm-c7HnmBmFQQQ4eWxwHXSB}
pwn.college{7lZS5NBUFJ..7oH1Gohjqsz7J58Zv96R3sm8waP.TSGnQsI}
pwn.college{Z0nsiPltG6U3iTYykZtI0cXq5uIbIbQ-9m3Il89hB3jUoYw}
pwn.college{1HC0cxX5fQ7qHM8y10ulNSCQaO.thyy-mHWzUcI26Hy3L1z}
pwn.college{BPV7BCmub3J9vj0jgPGaTKjPQgZm--j4b2bvJf-DpPg1456}
pwn.college{vYdvsiL9KSbpIkbcbvcqJ2P9tDQVwR96CoUWHAYwFugRBNl}
pwn.college{QJoSk4eZfARGwDP8TFFun9MuZktI7ohYDDGHTeYjfFz64Z1}
pwn.college{WH75U4llK2zKjt9U7A8mz38ixPlO-p9u5hKZPWujRtqONcn}
pwn.college{ISwUlU7z2KdSwtLQPJIMKDGfKmTbQDLWRsUb.lHn-9eQisL}
pwn.college{egw2uoGzlzraOyDNNzQByILLtwfkcsIZ8Pe7h.i0NG1jDYR}
pwn.college{-DXet.EjhxPYKGmq.g1ykl8V2UwMO-JVKbvzL78b1RPtz7V}
pwn.college{zVnCBTni3N7MvBwRLa7UowtPhf0.I2nXbihQrNBEoMyh-73}
pwn.college{pbDNrEdXJaluVCiNNvgpfH0s9RDZQcOQ6w2DsYZyhnP.3oL}
pwn.college{yJjLAy8PS2oTpIXvjGQ4.m5w.gv7a606OOYM0QS3qhOamhu}
pwn.college{dpUc0W-XsX1tEZdqt9evjgBZjWj8ymYjKshV-nHIRfGksCK}
pwn.college{IaDzbgrHCytOQq25xWoBZ8XtvvBRx2QCHLxVWCnalzWs1Hg}
pwn.college{GqqTMSjz.zraYxSIjrLjQ1dfnUOQjxziuNzOaVum5SlLihm}
pwn.college{XA2pD9CL9Mnj9s7eHp3RVzYfPhLN3S77Ix-Nzl2o.lI7buI}
pwn.college{cvpcSxRshlMmoimT5cPH9x6AEP65ty6cxDDaQelbVI7QM0W}
pwn.college{iVbHXi47v9wVU0yiXnIBDAVBHkwG2.VlAdWHPGolasBwzae}
pwn.college{Q3NpM.3tbCLYEke7jN4IiJGmShH.h6wvp-hdOHdVCYQobmH}
pwn.college{XSJM2DWdsUBgOVFSfdCFzNbCSjJLgTxlX9rI8tyTEf-7Q7u}
pwn.college{DPGfjWL1jmV38nZiOEdNulzxp7AsFfsT2WAleQxJvabYbvc}
pwn.college{O3CO56FCa1IT6iU-qahcwiLqDWxHb6NEIHU4DpKbhfq7L6p}
pwn.college{tfgyxrLMVrI9fouB3nw1ELBlSorNVyOgrXM8Y7glB16vlCr}
pwn.college{VMmbOTl3bfXCLua-PGyuykaYliNyzXNEx.ELfCbBfRL3QGF}
pwn.college{BxBpNiKezQCUybxTajVXO8RRjsb2pK-x0ZA7--BqnMtSRkn}
pwn.college{jxGpD3BpI4V9NLt0zKQbUJoeXbnvQ.FpwITWvoLTQAdradc}
pwn.college{niORkPNpQ.ZeGyZuvlV7a5Dyz8sWIolWm-BVuIfD-Xdpv--}
pwn.college{-nYFXiu1u85TTRyj-xI6rzIx2KOucSVxpARA5gwGoh1bWxu}
pwn.college{-53dba9-1Qrcj1UxIw58Jw.LpQlo3V8yyowBMvwM4Td42HZ}
pwn.college{hLDYqZL7CIC1MTeORiclLa01OkHryoqjBzerRv3MqzQ1Iav}
pwn.college{NTobTcDCJs4p4KHxdiIrJUWPJktwTwzrjn2YMJ4dNl2LR-7}
pwn.college{5HgOmGX.RS8pgX2-3r9o2T6Fbkvi2EXLciFJwSeE9XlpLwJ}
pwn.college{T6dPQ0DZFkj6tPJG2vw6pwtGTEX31M9QHx5xctniUu-bUgN}
pwn.college{YL1CyG7mkQ9Ytb7aj8SsefDS7xlIDJw9YqX5IBqMSy7fc7F}
pwn.college{ZdtwGCK-7rZMPRT9fwDxs.q41S6wgl5BUCsMcYph4A1uuAa}
pwn.college{uND6CHTcJ8CK4jJD3hhfOdaK1VxU.-Coc4t7L0qF7q.gdgP}
pwn.college{4RdznRpwLeMkZA.jBUSEhHxEV66xJbc-mDe.tlsIhH12yDj}
pwn.college{KY4cu345oUdJFmwER49scjOFc0vmEFb5Nqf86G-wcEeS57k}
pwn.college{EGwT63YG.FHPVR.DXC5bycXoUgcXP4Dh.RAVU2LAoVKpHdE}
pwn.college{2G-M7ADHd7NbG.uN3fqYXMSEVeALAvlcJD5niblkU-7j5rO}
pwn.college{kU5eMSNaQf8P-Nh8.dIsF4IwC8eq2MuOYXfFuxJS6gUdRzk}
pwn.college{H3.oaxD5vKp1GppUuSJf7c.oMXuNt1DCr.LZJbE.BTFylfM}
pwn.college{6EU5fJQfDI-myo4Ov4c3isZgwmFG11KzZ4z1qogOMoHnH3O}
pwn.college{MZM4RvIzZS4mHAJQWbVKKEYjWgj-hbq5dJvA.uN90bsqbrb}
pwn.college{28GXM2eFExuLk-NhYEIHCdDdJHHyEtMjB6u.g4vhgtmaHgb}
pwn.college{lvYrjcTV6sLS3NfsifGq1Rz..Q5oEo-MES9xoyaWwatzCDF}
pwn.college{wOlRQra3qa2kx-ID.L9wEkv-tr0-95T51VCbNvvFn7N3nNT}
pwn.college{dK11qrfuYfi6U2vhpb6l7dpq-mTG.Ppo0sEOIA.AFey2M0t}
pwn.college{N7A7rRHhaEXvnCyU.qITgx5JNCany-dxCPOOtCJlNw-Jrh0}
pwn.college{a1AHQalj9fYdB6gJ6yN7Ek6LLvPftFy2BkM8lmHhNK5.lCp}
pwn.college{FcijOj.0TJjzRyNuvH3Wr-GPRi7zdXpNQ-vqVxQ.E4vFd82}
pwn.college{y6pxukByAaNk8mnPWEypVyu0vlNWsIQ2sbimuJ.7QZP4A88}
pwn.college{rgFVE3t4XaBsSGUyrnZaLhb1PlEN03p2xvjpFTeLpOFGrWq}
pwn.college{wlGvsNXpZxfmpbas48QQ8QrylafFj6wS13sKlnRgbJBlHJ.}
pwn.college{dH89dVXWubxPi9D-x5rHGNKLGcFkmSMCh0XcO4Dwx.5a6GL}
pwn.college{5HGCh5uPf9KxCfON5YgCU-7JTgmfeezloWFwVxDGPWixkZT}
pwn.college{2mp1-AwFYNFeB-K6ExwCVCbEfGZPI.1PFMpe2bJ2n.iIbLg}
pwn.college{uUG.1jFUerY6rsuAOCA3OchhW8uypMLbAjeJwCU4JbpQ6FM}
pwn.college{yEcrZgznpanpNRasNtrHXBfNBxm1scsNpLdp2B1niORVbxm}
pwn.college{16eEVxblztoNnDCnaAuLQte-mlBVagrm32BsOT6nKiXZfgS}
^C
hacker@processes~killing-misbehaving-processes:~$ /challenge/run
Sending the flag to /tmp/flag_fifo!
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo
pwn.college{glDkcfo0ULrWybsv-Q2J-UDBs1L.0FNzMDOxwSOxkjNzEzW}
```

## What I Learn
It was just an application of the old concepts.
## References
None.
