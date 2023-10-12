
<div align="center">
  <img src="Fig/fl_vanet.png" alt="logo" width="350" height="auto" />
  <h1>FedComm</h1>
</div>
  
# 1 About FedComm
In ProVerif, we have provided the complete code to assist in verifying the primary security properties such as authentication and confidentiality.

## ProVerif
* Install [ProVerif 2.04](https://bblanche.gitlabpages.inria.fr/proverif/).
* Make sure that `ProVerif` is in your `PATH`.
* Fedcomm ProVerif source code in `ProVerif/proverif2.04/fedcomm.pv`.
* Enter the following code to obtain formal verification results.
  
~~~
./proverif fedcomm.pv
~~~

The verification results of ProVeif are as follows.

~~~
Verification summary:
Query not attacker(RID_n[]) is true.
Query not attacker(Para[]) is true.
Query not attacker(PID_n[]) is false.
Query not event(begin_TA_V) is false.
Query not event(end_TA_V(x1)) is false.
Query inj-event(end_TA_V(x2)) ==> inj-event(begin_TA_V) is true.
Query not event(begin_TA_RSU) is false.
Query not event(end_TA_RSU(x3)) is false.
Query inj-event(end_TA_RSU(x4)) ==> inj-event(begin_TA_RSU) is true.
Query not event(begin_V_RSU(x5)) is false.
Query not event(end_RSU_V(x6)) is false.
Query inj-event(end_RSU_V(x7)) ==> inj-event(begin_V_RSU(x8)) is true.
~~~

# Acknowledgements
The useful resources we use.
* [ProVerif](https://github.com/miculan/telegram-mtproto2-verification)
