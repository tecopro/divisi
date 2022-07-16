## Simbol Flowcharts
### Terminator
```mermaid
flowchart LR
    terminator(["Menandakan start (awal) atau end (akhir) program"])
```
### Arah Aliran
```mermaid
flowchart LR
    mulai([Start])-- Menunjukkan arah aliran proses pada program -->akhir([End])
    mulai2([Awal])-->akhir2([Akhir])
```
### Preparation
```mermaid
flowchart LR
    preparation{{Proses deklarasi atau pemberian nilai pada variabel yang digunakan}}
```
### Proses
```mermaid
flowchart LR
    proses[Menunjukkan proses yang dilakukan mesin komputer]
```
### Input/Output Data
```mermaid
flowchart LR
    io[/"Menandakan proses input/output data secara manual"/]
```
### Predefined Process (subprogram)
```mermaid
flowchart LR
    pp[[Menunjukkan proses subprogram]]
```
### Kondisi (Decision)
```mermaid
flowchart LR
    decision{"Menggambarkan sebuah \n keadaan/pemilihan dari dua kondisi \n yang bernilai true (benar) atau false (salah) \n untuk selanjutnya mengerjakan \n statement (pernyataan) tertentu"}
```
### On Page Connector
```mermaid
flowchart LR
    opc(("Menghubungkan bagian \n flowchart yang terpisah \n pada satu halaman"))
```
### Off Page Connector [^opc-note]
```mermaid
flowchart LR
    opc[\Menghubungkan bagian flowchart yang terputus pada halaman berbeda/]
```
<hr>

## Jenis Flowcharts
### System Flowcharts
```mermaid
flowchart LR
    s([Mulai]) -->
        income[/x = Pemasukan/] -->
        cost[/y = Pengeluaran/] -->
        decision{x > y}-- "&nbsp True &nbsp" -->
            profit[Laba = x - y] -->
            output_profit[Print Laba] --> e
        decision{x > y}-- "&nbsp False &nbsp" -->
            loss[Rugi = y - x] -->
            output_loss[Print Rugi] --> e
    e([Selesai])
```
### Data Flowcharts [^df-note]
```mermaid
flowchart LR
    R--"&nbsp Requisition &nbsp"-->
    RFQ--"&nbsp RFQ &nbsp"-->DNR
    DNR--"&nbsp Yes &nbsp"-->ERFQ-->DA
        DA-."&nbsp No &nbsp".->R
        DA--"&nbsp Yes &nbsp"-->RRFQ
    DNR-."&nbsp No &nbsp".->RRFQ
        RRFQ-->
        DDQ--"&nbsp Yes &nbsp"-->Q
            Q--"&nbsp Quote &nbsp"-->
            RQ-->DQA
            DQA--"&nbsp No, &nbsp \n &nbsp Send Quote Response &nbsp"-->RQR
            DQA--"&nbsp Yes &nbsp"-->O
                O--"&nbsp Order &nbsp"-->
                RO-->DOA
                DOA-."&nbsp No, &nbsp \n &nbsp Send Order Response and &nbsp \n &nbsp Revised Quote &nbsp".->RQ
                DOA--"&nbsp Yes &nbsp"-->FO
                    FO--"&nbsp Order Items &nbsp"-->
                    ROI--"&nbsp Delivery Note &nbsp"-->I
			      I--"&nbsp Invoice &nbsp"-->MP
                    ROI-->
			  MP-->RP

    subgraph Ship Officer
        R[Prepare Requisition]
    end
    subgraph Buyer Agent
        RFQ[Prepare Request for Quote]
        DNR{Need Review}
        RQ[Review Quote]
        DQA[Quote Acceptable]
        O[Prepare Order]
    end
    subgraph Superintendent
        ERFQ[Evaluate RFQ]
        DA{Approves}
    end
    subgraph Vendor
        RRFQ[Review RFQ]
        DDQ{Decides to Qutoe}
        Q[Prepare Qutoe]
        RQR[Review Quote Response]
        RO[Review Order]
        DOA{Order Acceptable}
        FO[Fullfill Order]
        I[Prepare Invoice]
        RP[Receive Payment]
    end
    subgraph Receiving Agent
        ROI[Receive Order Items]
        MP[Make Payment]
    end
```
### Website Flowcharts
```mermaid
flowchart LR
    h[Home]-->Aplikasi & Divisi & lj & lp & lhk & d{Token?}
    d -- "Yes" --> Blog
    d -- "No" --> Aplikasi --> Blog
    lj & lp -- "Informasi Lebih Lanjut" --> lhk

    subgraph Aplikasi
        ai[Sign In]
        ao[Sign Out]
    end
    subgraph Blog
        bk[Kategori]
        bpt[Postingan Terbaru]
        bt[Tags]
        bp[Penulis]
    end
    subgraph Divisi
        djv[Java]
        dw[Website]
        dg[Grafis]
        do[Office]
        djr[Jaringan]
        da[Animasi]
    end
    lj["Jadwal"]
    lp["Pendaftaran"]
    lhk["Hubungi Kami"]
```
[^opc-note]: Simbol dari Off Page Connector adalah segi lima terbalik. Karena bentuk ini tidak tersedia dalam bahasa mermaid, maka diilustrasikan sebagai trapesium.
[^df-note]: Versi penuh dari Data Flowcharts yang terlihat jelas, dapat diakses melalui [kroki.io](https://kroki.io/mermaid/svg/eNp9VMGOmzAQPSdfgfbQU9lPiETFIiFtADtSpYrmQMiQWGUxtQ2rKNp_r7GJbQjUlyjjN2_mvRlT1fSzvBZMeO9468mDff_lW3PirYfhb0c4EYQ2noq8-P5OYyJkURGyt2GiSeSvAfwCbgFvKnUXBgqmoIH_OiITOgJf_R12AYtUWFKZYosUD4BqWRe2rCFaprUpw7Eg1FEBMx8MudKEgklQ_jfJCf2uU73fo5feAZrzSIqBt7ThDjtGeJVr0m06gQ0nNcCUnYGtdKy6Toeu0-DpQsYcQ5c71-Sm80KGZjAMPeFwnhg3TAUt1ltUFz3LG0401xgL-OD_UarVxiYrhJr0wG5SnTvTeLvZbDTaYuOmp6R0UPtsnX-nGfbZMMNsq4C8O11Y0V69w5XIhqtKsjG7l3nGoC0YuM_tqK6lzVOCH91Nig0u0AibH6EJA3DhVZRp14923RN8T0BOY5gKfH7ZfJTr0FMGCnI9uqAsoRXFqXZuU1NUTWCl4UPXAiONkBduz8NHIH_ri7orhu2PkFM1uAdty2gP_GuZ86eMUDZ51w8FU6YQ3UMoyVkulKBSnaBgZVvT1MXR8QNPDDEr7kDSB8LRPu7xXS-ktcyWjNI86uq6InU9T4xNN-O2OcUyWawEua5eVtw-pI0rXmsUaS7zBUljw-C8Flthn-X74s8z_T_Xk6Eq)
