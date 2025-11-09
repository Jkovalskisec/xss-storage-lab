# XSS Stored – Flag Capturada  
**Jean Kovalski** | 09/11/2025  
**Curso:** Web Hacking na Prática (HackingClub)  
**Alvo:** 10.10.0.5  

---

## PASSO A PASSO (COMO EU FIZ)

1. **Testei comentários normais** → "Olá, isso é um test"  
2. **Testei formatação** → `<b>Teste em negrito</b>` → apareceu em **negrito**  
3. **Vi que o input era refletido sem filtro** → injetei o payload:  
   ```html
   <script>alert("XSS_STORED_BY_JEAN")</script>
