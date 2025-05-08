<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Nosso Amor</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
      body {
        background: linear-gradient(to top, #ffe4e6, #fff0f5);
      }
    </style>
  </head>
  <body class="flex items-center justify-center min-h-screen text-center p-6">
    <div class="bg-white rounded-2xl shadow-xl p-8 max-w-md w-full">
      <h1 class="text-3xl font-bold text-pink-600">Eu & Você 💖</h1>
      <p class="mt-4 text-gray-700 text-lg">Estamos juntos há:</p>
      <div id="contador" class="text-4xl font-semibold text-rose-500 mt-2"></div>

      <div class="mt-8 flex flex-col gap-4">
        <a
          href="https://wa.me/5511970510655"
          target="_blank"
          class="bg-pink-500 text-white py-3 rounded-xl shadow hover:bg-pink-600 transition"
        >
          🩷 Saudades dela
        </a>
        <a
          href="https://wa.me/5511970651612"
          target="_blank"
          class="bg-rose-500 text-white py-3 rounded-xl shadow hover:bg-rose-600 transition"
        >
          💙 Saudades dele
        </a>
      </div>
    </div>

    <script>
      // Data de início do relacionamento: 1 mês e 5 dias atrás
      const dataInicio = new Date();
      dataInicio.setMonth(dataInicio.getMonth() - 1);
      dataInicio.setDate(dataInicio.getDate() - 5);

      function atualizarContador() {
        const agora = new Date();
        const diff = agora - dataInicio;

        const dias = Math.floor(diff / (1000 * 60 * 60 * 24));
        const meses = Math.floor(dias / 30);
        const diasRestantes = dias % 30;

        document.getElementById("contador").textContent = `${meses} mês(es) e ${diasRestantes} dia(s)`;
      }

      atualizarContador();
      setInterval(atualizarContador, 60 * 1000); // atualiza a cada minuto
    </script>
  </body>
</html>
