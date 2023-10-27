# in-memory cache

in-memory cache - это Go пакет, предоставляющий простую и эффективную реализацию in-memory кеша для вашего приложения. Этот кеш позволяет хранить значения в памяти и обеспечивает доступ к ним через ключи. Пакет cache предоставляет методы для добавления, получения и удаления значений из кеша.

## Установка

Для установки пакета, выполните следующую команду:

go get -u github.com/mtamerlan/cache

## Использование

```go
package main

import (
    "fmt"
    "github.com/mtamerlan/cache"
)

func main() {
	cache := cache.New()

	cache.Set("userId", 42)
	userId := cache.Get("userId")

	fmt.Println(userId)

	cache.Delete("userId")
	userId := cache.Get("userId")

	fmt.Println(userId)
}