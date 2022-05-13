<template>
  <div>
    <div class="card">
      <div class="card-body">
        <div class="info mb-3">Aramanıza uygun sonuç bulunamadı.</div>
        <div class="explain">
          Bu aramana uygun bir ilan yayınlanırsa sana haber vermemizi
          ister misin?
        </div>
      </div>
    </div>
    <div class="mt-5 mb-2 font-weight-bold">
      Doğru sonuçlara ulaşmak için şunlara dikkat etmelisin:
    </div>
    <ul>
      <li>Yazım yanlışı yapmadığından emin olmalısın.</li>
      <li>
        Daha genel kullanıma sahip kelimeler kullanabilirsin. (Örn: "HR"
        yerine "İK" ya da "İnsan Kaynakları")
      </li>
      <li>
        Daha farklı kelimeler kullanabilirsin. (Örn: "Yazılımcı" yerine
        "Backend Yazılım Uzmanı")
      </li>
      <li>
        Kısaltma kullanmak yerine, kelimeleri açık şekilde yazabilirsin.
        (Örn: "Müh" yerine "Mühendis")"
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "NoContent"
};
</script>

<style scoped>
.card {
  color: #185d68;
  background-color: #d1ecf1;
  border: 1px solid transparent;
  border-radius: 3px;
}
</style>
