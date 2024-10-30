## Plane Wave Model
Merujuk pada tulisan Viljanen 1998, medan listrik arah $y$ yang dibangkitkan oleh gangguan medan magnet saat badai adalah:
$$
    E_y(t) = -\dfrac{1}{\sqrt{\pi\mu_0\sigma}}\int_{-\infty}^{t}\dfrac{g_x(u)}{\sqrt{t-u}}
$$
dengan 
$$
    g_x(u) = \dfrac{dH}{du}
$$
serta beberapa konstant sebagai berikut:
$$
    \pi = 3.1415\newline
    \mu_0 = 1.2566\times10^{-3}\ \text{NA}^{-2}
$$

Misalnya kita gunakan Quebec earth model untuk tebakan awal, maka resistivitas Bumi adalah $\rho=1000\ \Omega\text{m}$ dan konduktivitasnya adalah $\sigma=10^{-3}\ \text{S/m}$.

Nilai koefisien di luar integral bisa kita nyatakan sebagai
$$k=\dfrac{1}{\sqrt{\pi\mu_0\sigma}}=1.5916\times10^{4}\ \text{ms}^{-1/2}$$

Pada prakteknya, kita punya data medan magnet dengan resolusi 1 menit, sehingga perhitungan $E_y$ pada waktu $t$ kita bisa dekati dengan mengintegrasikan $g_x(u)$ selama 10 menit sebelumnya, yakni:

$$
    E_y(t) = -k\left[ \dfrac{g_x(t-30)}{\sqrt{30}} + \dfrac{g_x(t-90)}{\sqrt{90}}+\ldots+
    \dfrac{g_x(t-510)}{\sqrt{570}}\right]
$$
Dengan formulasi di atas, satuan dari bagian dalam kurung siku (bagian integral) adalah nT $\text{s}^{-3/2}$. Setelah dikalikan dengan $k$, satuan dari $E_y$ adalah nT m/s atau setara dengan $10^{-3}$ mV/km.

Perlu dicatat bahwa $g_x(u)$ dinyatakan dalam nT/s dan dihitung di titik tengah interval data magnetometer. Misalnya kita punya $H(t=0\text{ min})=40116$ nT dan $H(t=1\text{ min})=40119$ nT, maka kita bisa hitung 
$$g_x(t=0.5\text{ min})=3\text{ nT/min}=0.05\text{ nT/s}$$

Maka dari itu, nilai $u$ pada fungsi di atas adalah $u=[0.5, 1.5, \ldots, 9.5]\text{ min}$ atau $u=[30, 90, \ldots, 570]\text{ sec}$.
## Tabel konversi

Berikut adalah beberapa hubungan yang perlu diingat dalam melakukan konversi satuan.
| Relasi | Formula |
| --- | --- |
| Watt, Newton | $W=N m/s$ |
| Watt, Volt, Ampere | $W = VA$ |
| Volt, Ampere, Ohm | $V=A\Omega$ |
| Tesla, Volt | $T=Vs/m^2$ |
