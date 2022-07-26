<h1 class="code-line" data-line-start=0 data-line-end=1 ><a id="Github101_Trke_Dkmantasyon_0"></a>Github101 Türkçe Dökümantasyon</h1>
<h2 class="code-line" data-line-start=1 data-line-end=2 ><a id="ehir_Teknolojileri_Birimi_in_Hazrlanmtr_Genel_Kullanma_Aktr_1"></a>Şehir Teknolojileri Birimi İçin Hazırlanmıştır. Genel Kullanıma Açıktır.</h2>
<p class="has-line-data" data-line-start="3" data-line-end="4">İçindekiler</p>
<ul>
<li class="has-line-data" data-line-start="5" data-line-end="6">Git Nedir?</li>
<li class="has-line-data" data-line-start="6" data-line-end="7">Git’e Neden İhtiyaç Duyarız?</li>
<li class="has-line-data" data-line-start="7" data-line-end="8">Git’in Çalışma Mantığı</li>
<li class="has-line-data" data-line-start="8" data-line-end="9">Git’in Yapılandırması</li>
<li class="has-line-data" data-line-start="9" data-line-end="10">Git Projesi Oluşturma</li>
<li class="has-line-data" data-line-start="10" data-line-end="11">Dosyaları Git Deposuna (Repository) Ekleme</li>
<li class="has-line-data" data-line-start="11" data-line-end="12">Git Dosyasındaki Değişiklikler</li>
<li class="has-line-data" data-line-start="12" data-line-end="13">Git’ten Dosya Silme</li>
<li class="has-line-data" data-line-start="13" data-line-end="14">Projedeki Dosyanın İsmini Değiştirme</li>
<li class="has-line-data" data-line-start="14" data-line-end="15">Dosya Taşıma</li>
<li class="has-line-data" data-line-start="15" data-line-end="16">Dosyadaki Değişiklikleri Geri Alma</li>
<li class="has-line-data" data-line-start="16" data-line-end="17">Versiyon Değiştirme</li>
<li class="has-line-data" data-line-start="17" data-line-end="18">Git Dallanma (Branch)</li>
<li class="has-line-data" data-line-start="18" data-line-end="19">Uzak Repo’dan Local’e Proje Çekme (Clone)</li>
<li class="has-line-data" data-line-start="19" data-line-end="20">Uzak Repodan Değişiklikleri Local Repoya Çekmek (Pull komutu)</li>
<li class="has-line-data" data-line-start="20" data-line-end="21">GitHub Nedir?</li>
<li class="has-line-data" data-line-start="21" data-line-end="22">GitHub Neden Kullanılır?</li>
<li class="has-line-data" data-line-start="22" data-line-end="23">GitHub Repository (Depo) Oluşturma</li>
<li class="has-line-data" data-line-start="23" data-line-end="24">GitHub’a Proje Gönderme</li>
<li class="has-line-data" data-line-start="24" data-line-end="25">GitHub Branch</li>
<li class="has-line-data" data-line-start="25" data-line-end="26">GitHub Issues</li>
<li class="has-line-data" data-line-start="26" data-line-end="28">Github Issue Closed</li>
</ul>
<h2 class="code-line" data-line-start=28 data-line-end=29 ><a id="Git_Nedir_28"></a>Git Nedir</h2>
<p class="has-line-data" data-line-start="30" data-line-end="31">Bir versiyon kontrol sistemidir. Yapacağınız projelerin kopyalarını alarak projelerinizin eski versiyonlarına kolaylıkla geri dönmenizi sağlayan bir sistemdir.</p>
<blockquote>
<p class="has-line-data" data-line-start="33" data-line-end="34">Git sistemi, Linux çekirdeğini yazan Linus Torvalds tarafından geliştirilmiştir. Açık kaynak kodlu özgür yazılım ürünüdür.</p>
</blockquote>
<h2 class="code-line" data-line-start=35 data-line-end=36 ><a id="Git_alma_Mant_35"></a>Git Çalışma Mantığı</h2>
<p class="has-line-data" data-line-start="37" data-line-end="38">Git çalışma mantığı olarak diğer versiyon kontrol sistemlerinden biraz farklıdır. Diğer versiyon kontrol sistemleri, commit işleminde dosyaların değişiklik durumuna göre yeni versiyon kopyasında dosyanın durumunu kaydeder. Ancak git’te her versiyon için projenin tamamının durumu kaydedilir. Çalışma alanı olarak üçe ayrılmaktadır. Çalışma dizinimizde (working directory) git projesi başlatarak işe koyuluruz. Bu alan sistemin ilk alanıdır. Daha sonra çalışma dizinimizdeki dosyaları geçiş bölgesine (staging area) ekleriz. Bu alan sistemin ara alanıdır.</p>
<h2 class="code-line" data-line-start=39 data-line-end=40 ><a id="Git_Yaplandrmas_39"></a>Git Yapılandırması</h2>
<p class="has-line-data" data-line-start="41" data-line-end="42">-1- Kullanıcı Adı Belirleme.</p>
<pre><code class="has-line-data" data-line-start="43" data-line-end="45" class="language-sh">git config --global user.name “username”
</code></pre>
<p class="has-line-data" data-line-start="45" data-line-end="46">-2- E-mail Belirleme</p>
<pre><code class="has-line-data" data-line-start="48" data-line-end="50" class="language-sh">git config --global user.email “email_adress”
</code></pre>
<h2 class="code-line" data-line-start=51 data-line-end=52 ><a id="Git_Projesi_Oluturma_51"></a>Git Projesi Oluşturma</h2>
<p class="has-line-data" data-line-start="53" data-line-end="54">Proje klasörünün bulunduğu konuma giderek projeyi <code>git init</code> komutuyla oluşturabilirsiniz</p>
<h2 class="code-line" data-line-start=56 data-line-end=57 ><a id="Dosyalar_Git_Deposuna_Repository_Ekleme_56"></a>Dosyaları Git Deposuna (Repository) Ekleme</h2>
<p class="has-line-data" data-line-start="58" data-line-end="59">Repository Git projenizin Git tarafından saklandığı yerdir.</p>
<pre><code class="has-line-data" data-line-start="61" data-line-end="64" class="language-sh">git add .
git commit -m <span class="hljs-string">"first commit"</span>
</code></pre>
<p class="has-line-data" data-line-start="65" data-line-end="66">Projenizin bir versiyon kopyasını oluşturmuş oldunuz. Birinci satırdaki ‘add‘ komutu dosyaları geçiş bölgesine (staging area) yükle anlamına geliyor.  Add komutunun yanındaki nokta çalışma alanındaki tüm dosyaları geçiş bölgesine gönder anlamına gelir eğer siz belli bir dosya göndermek istiyorsanız o dosyanın adını yazabilirsiniz.</p>
<p class="has-line-data" data-line-start="67" data-line-end="68">Projede en az bir kere yukardaki yöntem ile repoya dosya yüklediyseniz ve bundan sonra dosyalarınızı geçiş bölgesine eklemeden direk repoya atmak istiyorsanız aşağıdaki kod bloğunu kullanabilirsiniz.</p>
<p class="has-line-data" data-line-start="69" data-line-end="70"><code>git commit -am &quot;first commit&quot;</code></p>
<p class="has-line-data" data-line-start="71" data-line-end="72">Log kayıtlarını görüntülemek</p>
<pre><code class="has-line-data" data-line-start="73" data-line-end="75" class="language-sh">git <span class="hljs-built_in">log</span>
</code></pre>
<h4 class="code-line" data-line-start=76 data-line-end=77 ><a id="Git_Dosyasndaki_Deiiklikler_76"></a>Git Dosyasındaki Değişiklikler</h4>
<p class="has-line-data" data-line-start="78" data-line-end="79"><code>status</code> komutu, çalışma dizininin durumunu ve hazırlama alanını görüntüler.  Hangi değişikliklerin hazırlandığını, hangilerinin yapılmadığını ve hangi dosyaların Git tarafından izlenmediğini görmenizi sağlar.</p>
<pre><code class="has-line-data" data-line-start="80" data-line-end="82" class="language-sh">git status
</code></pre>
<p class="has-line-data" data-line-start="83" data-line-end="84"><code>diff</code> komutu, çalışma dizinin durumunu ve hazırlanma alanını satır şeklinde görüntülemenizi sağlar. Sadece belirli dosyalardaki değişikliğe bakmak için dosyanın uazntısını eklemelisiniz.</p>
<pre><code class="has-line-data" data-line-start="86" data-line-end="88" class="language-sh">git diff
</code></pre>
<p class="has-line-data" data-line-start="88" data-line-end="89"><code>git diff dirctory/</code></p>
<h2 class="code-line" data-line-start=90 data-line-end=91 ><a id="Gitten_Dosya_Silme_90"></a>Git’ten Dosya Silme</h2>
<p class="has-line-data" data-line-start="92" data-line-end="93">Git projesinden dosya silmek için iki tane yöntem var. Birincisi direkt çalışma dizininden silmek, ikincisi ise komutlar ile silmek.</p>
<p class="has-line-data" data-line-start="94" data-line-end="95">Birincisini anlatarak başlıyorum. Proje dosyanıza giderek dosyanızı siliyorsunuz. Ve sırasıyla aşağıdaki komutları yazarak silme işlemini gerçekleştirmiş olursunuz.</p>
<pre><code class="has-line-data" data-line-start="98" data-line-end="101" class="language-sh">git rm  rm_file/
git commit -m <span class="hljs-string">"file deleting”
</span></code></pre>
<h2 class="code-line" data-line-start=101 data-line-end=102 ><a id="Git_Dosya_smi_Deitirme_101"></a>Git Dosya İsmi Değiştirme</h2>
<pre><code class="has-line-data" data-line-start="104" data-line-end="107" class="language-sh">git mv file_first_name last_name
git commit -m “name change”
</code></pre>
<h2 class="code-line" data-line-start=107 data-line-end=108 ><a id="Git_Dosya_Tama_107"></a>Git Dosya Taşıma</h2>
<pre><code class="has-line-data" data-line-start="110" data-line-end="113" class="language-sh">git mv filenameToMove destinationFolder
git commit -m “Migration process”
</code></pre>
<h2 class="code-line" data-line-start=114 data-line-end=115 ><a id="Dosyadaki_Deiiklikleri_Geri_Alma_114"></a>Dosyadaki Değişiklikleri Geri Alma</h2>
<p class="has-line-data" data-line-start="116" data-line-end="117">Dosyada yapılan değişiklikleri geri almak</p>
<pre><code class="has-line-data" data-line-start="119" data-line-end="121">git checkout -- changed_filename
</code></pre>
<p class="has-line-data" data-line-start="122" data-line-end="123">Dosyaları <code>git add</code> ile ekledikten sonraki değişiklikleri geri almak</p>
<pre><code class="has-line-data" data-line-start="125" data-line-end="128">git reset HEAD file_name 
git checkout -- file_name
</code></pre>
<h2 class="code-line" data-line-start=128 data-line-end=129 ><a id="Versiyon_Deitirme_128"></a>Versiyon Değiştirme</h2>
<p class="has-line-data" data-line-start="130" data-line-end="131">Bu işlem için git log ile versiyonları sıralıyoruz ve gitmek istediğimiz versiyonun hash kodunu alıyoruz. (Hash code, commit yazısının yanında bulunan kod satırıdır.)</p>
<pre><code class="has-line-data" data-line-start="133" data-line-end="136">git checkout version_hash_code -- .
git commit – m “old version copied”
</code></pre>
<h2 class="code-line" data-line-start=136 data-line-end=137 ><a id="Git_Branch_136"></a>Git Branch</h2>
<p class="has-line-data" data-line-start="137" data-line-end="138">Git projesi oluşturduğunuzda varsayılan olarak main brach oluşur ve siz bu dal üzerinden işlemlerinizi gerçekleştirirsiniz. Bireysel çalışılan bir projede bu yöntem ile bir sıkıntı yaşamazsınız. Ancak çoklu projelerde çalışıyorsanız ve takım üyeleri projenin farklı alanları ile ilgileniyorsa o zaman sıkıntı yaşamaya başlayabilirsiniz. Branch sayesinde her takım üyesi kendi branch‘ında çalışarak diğer takım arkadaşlarının kodlarında değişikliğe sebebiyet vermez. Proje bitiminde merge işlemi ile tüm proje branch’ları master branch’ında birleştirilebilir.</p>
<ul>
<li class="has-line-data" data-line-start="139" data-line-end="140">Branch Listesini Görme</li>
</ul>
<pre><code class="has-line-data" data-line-start="141" data-line-end="144">git branch
Not : Aktif olan branch * sembolü ile gösterilir
</code></pre>
<ul>
<li class="has-line-data" data-line-start="144" data-line-end="145">Yeni Branch Oluşturma</li>
</ul>
<pre><code class="has-line-data" data-line-start="146" data-line-end="148">git branch new_branch_name
</code></pre>
<ul>
<li class="has-line-data" data-line-start="148" data-line-end="149">Oluşturulan Branch’a Geçiş Yapmak</li>
</ul>
<pre><code class="has-line-data" data-line-start="150" data-line-end="152">git checkout new_branch_name
</code></pre>
<p class="has-line-data" data-line-start="152" data-line-end="153"><strong>Hem branch oluşturup hem de branch’a geçiş yapmak istiyorsanız aşağıdaki kodu kullanabilirsiniz.</strong></p>
<pre><code class="has-line-data" data-line-start="154" data-line-end="156">git checkout -b new_branch_name
</code></pre>
<ul>
<li class="has-line-data" data-line-start="156" data-line-end="157">Branch’ın İsmini Değiştirmek</li>
</ul>
<pre><code class="has-line-data" data-line-start="158" data-line-end="160">git branch -m new_branch_name newBranch
</code></pre>
<ul>
<li class="has-line-data" data-line-start="160" data-line-end="161">Branch Silmek</li>
</ul>
<pre><code class="has-line-data" data-line-start="162" data-line-end="164">git branch -D newBranch
</code></pre>
<ul>
<li class="has-line-data" data-line-start="165" data-line-end="167">Branch’ları Birleştirmek (Merge)</li>
</ul>
<pre><code class="has-line-data" data-line-start="168" data-line-end="170">git merge master newBranch
</code></pre>
<h2 class="code-line" data-line-start=171 data-line-end=172 ><a id="Uzak_Git_Sunucusundan_HTTP_proje_ekmek_171"></a>Uzak Git Sunucusundan HTTP proje çekmek</h2>
<pre><code class="has-line-data" data-line-start="174" data-line-end="178">git clone https://github.com/username/your_git_repo
`örneğin`
git clone https://github.com/kadirbelkuyu/try.git
</code></pre>
<h2 class="code-line" data-line-start=178 data-line-end=179 ><a id="Deiiklikleri_local_sunucunuza_ekmek_178"></a>Değişiklikleri local sunucunuza çekmek</h2>
<pre><code class="has-line-data" data-line-start="181" data-line-end="184">git pull
git pull 'remote_address' 'branch_name'
</code></pre>
<h1 class="code-line" data-line-start=185 data-line-end=186 ><a id="Github_Proje_Gnderme_185"></a>Github Proje Gönderme</h1>
<pre><code class="has-line-data" data-line-start="188" data-line-end="194">git init
git add .
git commit -m “first commit”
git remote add origin repository_name.git
git push -u origin main
</code></pre>