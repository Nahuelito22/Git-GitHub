# 🍒 `git cherry-pick`

`git cherry-pick` es un comando avanzado que permite **aplicar un commit específico** de otra rama en tu rama actual, sin necesidad de hacer un merge completo.

---

## 🧠 ¿Cuándo usar `cherry-pick`?

- Querés traer un cambio puntual de otra rama (sin mezclar todo su historial).
- Necesitás aplicar un hotfix que ya hiciste en otra rama.
- Querés recuperar un commit específico sin hacer rebase o merge.

---

## 🛠️ Sintaxis básica

```bash
git cherry-pick <hash-del-commit>
```

Por ejemplo:
```bash
git cherry-pick a1b2c3d
```
Esto traerá ese commit (identificado por su hash) a tu rama actual.

---

## 📌 Pasos típicos
1. Estás en la rama main y querés traer un commit desde develop.
2. Buscás el hash del commit:
```bash
git log develop
```
3. Copiás el hash (por ejemplo, 3e8f9a1) y hacés el cherry-pick:
```bash
git checkout main
git cherry-pick 3e8f9a1
```

---


## ⚠️ Posibles conflictos
Si hay conflictos al aplicar el commit, Git te lo informará y deberás resolverlos manualmente:
```bash
# Resolver conflictos en los archivos afectados
git add <archivo-resuelto>

# Finalizar el cherry-pick
git cherry-pick --continue
```
También podés abortarlo si te arrepentís:
```bash
git cherry-pick --abort
```

---

## ✅ Consejos útiles

* Siempre revisá en qué rama estás antes de hacer cherry-pick.
* Podés cherry-pickear varios commits juntos:
```bash
git cherry-pick hash1 hash2 hash3
```
* Es ideal para casos puntuales, no para flujos de trabajo regulares.

---

## 🧪 Ejemplo práctico
```bash
git checkout hotfix
git cherry-pick 1a2b3c4
```
Trae un commit específico (por ejemplo, una corrección urgente) desde otra rama.


---


Usá cherry-pick con cuidado y sabiendo qué estás haciendo.
Es una herramienta poderosa, pero mal usada puede complicar tu historial.

---